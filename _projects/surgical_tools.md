---
layout: page
title: Surgical Tool Detection and Phase Estimation
description: A deep learning pipeline for real-time tool tracking and surgical phase recognition.
img: assets/img/surgery_tool.gif
importance: 1
category: Medical AI
selected: true  # Add this line
---
<div class="project-metadata">
    <strong>Year:</strong> 2021 – 2026 <br>
    <strong>Workplace:</strong> <a href="https://www.mteg.co.kr/" target="_blank">MTEG</a></div>

---
### Project Overview

This project implements a robust computer vision pipeline designed to automate the analysis of surgical videos. By combining state-of-the-art object detection with temporal sequence modeling, the system identifies surgical instruments and estimates the current phase of the procedure.

The workflow follows a two-stage architecture:
1.  **Tool Detection:** Real-time identification of 25 different surgical tools.
2.  **Phase Estimation:** Temporal analysis of tool presence to determine the surgical stage.

### Technical Workflow

The video stream is sampled at **1 FPS** (one frame per second). For each extracted frame, the detection models identify the presence of tools. Results are exported in the standard **Cholec80 format**, utilizing a binary encoding (1 for presence, 0 for absence) for each of the 25 tool categories.

Following detection, the binary sequences are processed through a temporal model to estimate the surgical phase, leveraging the chronological order of tool usage to improve accuracy.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/surgery_tool.gif" title="Real-time Detection" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Real-time multi-tool detection using YOLO/RT-DETR variants on live surgical feeds.
</div>

### Dataset & Performance

The models were trained on a massive, high-variance dataset to ensure generalization across different operating environments and surgeons.

* **Dataset Size:** 306,780 total annotated images.
* **Diversity:** Data sourced from multiple surgeries performed by various surgeons.
* **Scope:** 25 unique surgical instruments tracked.
* **Accuracy:** Achieved an average **mAP of 0.87** across all detection frameworks.

### Models Evaluated

To find the optimal balance between inference speed and detection precision, several architectures were benchmarked:

| Model Type | Architectures |
| :--- | :--- |
| **Object Detection** | YOLO, Faster R-CNN, DETR, RT-DETR |
| **Temporal Modeling** | Bi-LSTM, GRU |

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/insight.png" title="Phase and Tool Output" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Final system output showcasing the synchronized detection of tools and the resulting phase estimation.
</div>

### Key Contributions
* **Sampling Strategy:** Optimized frame extraction at 1-second intervals for computational efficiency.
* **Standardized Output:** Full compatibility with the Cholec80 dataset format for academic and clinical benchmarking.
* **Temporal Intelligence:** Using Bi-LSTM/GRU to understand the *context* of the surgery, not just individual frames.
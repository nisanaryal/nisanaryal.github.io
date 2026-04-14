---
layout: page
title: Emergency Room Operations Logging & De-identification
description: Automating Emergency Room operational logging through multi-object tracking and privacy-preserving video analysis.
img: assets/img/ajou_detect.gif
importance: 2
category: Medical AI
---

<div class="project-metadata">
    <strong>Year:</strong> 2023 - 2026 <br>
    <strong>Workplace:</strong> <a href="https://www.mteg.co.kr/" target="_blank">MTEG</a>
</div>

---

### Project Overview
This project focuses on automating the logging of key clinical events in an Emergency Room (ER) setting. To digitize ER operations, the system detects medical equipment and personnel, tracks their movements, and identifies critical timestamps for database entry.

A significant challenge of this project was **Patient & Staff Privacy**. I developed and deployed a dual-stage pipeline:
1.  **De-identification:** Real-time face detection and blurring to comply with medical privacy standards.
2.  **Event Analysis:** Object detection and tracking to log operational workflow.

### The "No-Internet" Challenge
Midway through the project, de-identification became an urgent requirement. **In just one week**, I completed the entire lifecycle—annotation, training, and deployment—locally within the hospital. Because the deployment site had no internet access for security reasons, the entire environment had to be configured and the model optimized strictly on-site.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/ajou_blur.gif" title="Face De-identification" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/ajou_detect.gif" title="Object Detection & Tracking" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: Automated de-identification pipeline (face blurring). Right: Real-time object detection and tracking for ER event logging.
</div>

### Technical Specifications
* **Detection Architectures:** YOLO, Faster R-CNN, DETR, RT-DETR.
* **Capabilities:** Multi-object tracking (MOT) for equipment and personnel to identify interaction-based events.
* **Deployment:** On-premise hospital servers with high-security (no-internet) constraints.
* **Rapid Prototyping:** Transitioned from raw data to a deployed de-identification model in 7 days.

### Impact
* **Operational Efficiency:** Replaced manual logging with automated, timestamped event entries.
* **Privacy Compliance:** Enabled the use of AI analysis in a sensitive clinical environment by ensuring 100% on-device de-identification.

<div class="skills-used">
    <strong>Key Tech:</strong> 
    <span class="badge badge-light">On-Premise AI</span>
    <span class="badge badge-light">Face Blurring</span>
    <span class="badge badge-light">Object Tracking</span>
    <span class="badge badge-light">Edge Deployment</span>
</div>
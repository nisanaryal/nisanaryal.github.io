---
layout: page
title: Optimal View Detection for Supraclavicular Block (SCB)
description: A two-stage computer-aided diagnosis (CADx) system to assist non-experts in identifying optimal ultrasound views for regional anesthesia.
img: assets/img/Ultrasound.gif
importance: 1
category: Medical AI
selected: true  # Add this line

---

<div class="project-metadata">
    <strong>Year:</strong> 2023 <br>
    <strong>Workplace:</strong> <a href="https://www.mteg.co.kr/" target="_blank">MTEG</a>

</div>

---

### Project Overview
Successful ultrasound-guided supraclavicular blocks (SCB) depend heavily on the clinician's ability to identify "sonoanatomy" in real time. For non-experts, this is a significant barrier. This project developed a CADx system that classifies whether a current ultrasound frame represents the **Optimal View** for a complete block.

The study utilized a large-scale retrospective dataset from **881 patients**, making it one of the most robust deep-learning evaluations for this specific clinical procedure.

### System Architecture
The project explored two distinct deep learning strategies to determine which approach best serves real-time clinical decision-making:

1.  **Classification Approach:** Utilizing **ResNet34** combined with **Gated Recurrent Units (GRU)** to incorporate temporal information from the ultrasound video stream.
2.  **Segmentation-to-Classification:** A cascade structure where a **U-Net** first segments the anatomy, which is then used as input for the classification network.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/Ultrasound.gif" title="Real-time Ultrasound Segmentation" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/ultrasound_architecture.png" title="Model Pipeline" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: Real-time inference showing sonoanatomy identification. Right: The two-stage architecture logic (U-Net + ResNet) used for optimal view determination.
</div>

### Key Findings & Technical Specs
* **Backbone Networks:** ResNet34 (Classification) and U-Net (Segmentation).
* **Performance:** The classification-first approach (ResNet34 + GRU) outperformed the segmentation-cascade, achieving an **AUROC of 0.936** and an average accuracy of **0.901**.
* **Temporal Integration:** The inclusion of GRU allowed the model to understand the movement and orientation of the ultrasound probe, which is critical for identifying the "optimal" slice of anatomy.
* **Data Scale:** Developed using a training/validation set of 600 patients and a blinded test set of 281 patients.

### Impact
* **Clinical Accessibility:** Demonstrated that AI can bridge the gap for non-expert clinicians, providing real-time guidance during regional anesthesia.
* **Academic Recognition:** Published in *Scientific Reports*, validating the methodology and the importance of temporal data in medical ultrasound analysis.

<div class="skills-used">
    <strong>Key Tech:</strong> 
    <span class="badge badge-light">ResNet</span>
    <span class="badge badge-light">GRU (Temporal Modeling)</span>
    <span class="badge badge-light">U-Net</span>
    <span class="badge badge-light">Medical CADx</span>
</div>


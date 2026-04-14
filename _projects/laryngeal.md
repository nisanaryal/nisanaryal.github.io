---
layout: page
title: Laryngeal Cancer Segmentation via Modified Attention U-Net
description: Precision semantic segmentation of laryngeal malignancies and anatomical structures using an Attention-gated Nested U-Net.
img: assets/img/larynx_result_1.png
importance: 2
category: Medical AI
---

<div class="project-metadata">
    <strong>Year:</strong> 2022 <br>
    <strong>Role:</strong> AI Research Engineer <br>
    <strong>Target:</strong> Malignant Tissue & Anatomical Regions<br>
    <strong>Workplace:</strong> <a href="https://www.mteg.co.kr/" target="_blank">MTEG</a>

</div>

---

### Project Overview
Early detection and boundary definition of laryngeal cancer are critical for surgical planning and radiation therapy. This project utilizes a **Modified Attention U-Net** to automatically segment cancerous regions and surrounding healthy anatomy from endoscopic and medical imaging of the larynx.

The model is specifically tuned to handle the irregular shapes and subtle texture differences characteristic of laryngeal tumors, providing clinicians with a clear visual map of the disease's extent.

### Architecture: Attention-Gated X-Net
Building on the success of nested architectures, this project employs a modified U-Net with integrated **Attention Gates**. This allows the model to:
* **Isolate Malignancy:** Focus high-dimensional feature extraction on the tumorous regions (represented in **pink**) while filtering out background noise from endoscopic light reflections.
* **Preserve Anatomical Context:** Simultaneously segment the surrounding laryngeal structures to provide a spatial reference for the clinician.

<div class="row justify-content-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/larynx_result_1.png" title="Laryngeal Segmentation Result 1" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="row justify-content-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/larynx_result_2.png" title="Laryngeal Segmentation Result 2" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Segmentation Comparison: (Left) Original Laryngeal Image, (Middle) Predicted Segmentation, (Right) Ground Truth. Cancerous regions are highlighted in <strong>pink</strong>.
</div>

### Technical Specifications
* **Architecture:** Modified X-Net (Nested U-Net) with Attention Gates.
* **Evaluation:** Performance measured by Mean Intersection over Union (mIoU) and Pixel Accuracy.

### Impact
* **Clinical Visualization:** High-contrast color-coding (Pink for Cancer) allows for immediate visual confirmation of the AI's diagnostic findings.
* **Surgical Guidance:** Provides reproducible, objective measurements of tumor area, assisting in more accurate staging and longitudinal monitoring.

<div class="skills-used">
    <strong>Key Tech:</strong> 
    <span class="badge badge-light">Attention U-Net</span>
    <span class="badge badge-light">Oncology AI</span>
    <span class="badge badge-light">Laryngeal Analysis</span>
    <span class="badge badge-light">Semantic Segmentation</span>
</div>
---
layout: page
title: Automated Laryngeal Airway Obstruction Analysis
description: Quantifying upper airway contraction and vocal cord dynamics through real-time semantic segmentation and signal processing.
img: assets/img/Dice.gif
importance: 1
category: Medical AI
selected: true  # Add this line

---

<div class="project-metadata">
    <strong>Year:</strong> 2024 <br>
    <strong>Workplace:</strong> <a href="https://www.mteg.co.kr/" target="_blank">MTEG</a>

</div>

---

### Project Overview
Airway obstruction monitoring typically requires manual review of endoscopic footage, which is subjective and time-consuming. This project automates the quantification of airway patency by segmenting critical laryngeal structures and calculating contraction ratios during the respiratory cycle.

The system processes vocal cord videos to track the dynamic area of the airway, providing clinicians with objective data to diagnose conditions like laryngomalacia or vocal cord dysfunction.

### Methodology & Pipeline
The analysis follows a three-stage clinical pipeline:
1.  **Multi-Class Segmentation:** Identifying the **Epiglottis**, **Tongue Base**, **Posterior Lateral Walls**, and the **Airway** lumen.
2.  **Temporal Area Mapping:** Extracting the pixel-wise area of the airway across all frames to generate a periodic respiratory waveform.
3.  **Obstruction Quantification:** Post-processing the waveform to identify peak (inhalation) and trough (contraction) points to calculate the percentage of airway closure.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/Dice.gif" title="Laryngeal Segmentation" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/Dice_result.png" title="Airway Area Waveform" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: Multi-class segmentation of the laryngeal space. Right: Resultant airway area plot used to calculate contraction ratios.
</div>

### Technical Specifications
* **Architecture Benchmarking:** Evaluated **YOLO** (for real-time bounding), **SegFormer**, and a **Modified U-Net with Attention gates** to prioritize edge-case boundary precision.
* **Signal Processing:** Implemented peak-finding algorithms on the area-time graph to filter respiratory noise and isolate valid breathing cycles.
* **Metrics:** Optimized for Dice Coefficient and mIoU to ensure the segmented airway area remains anatomically accurate across varying endoscopic light conditions.

### Impact
* **Objective Diagnostics:** Converted qualitative "visual guesses" of airway blockage into a concrete ratio (e.g., 40% obstruction).
* **Surgical Decision Support:** Provides a reproducible baseline for pre- and post-operative comparisons in laryngeal surgery.

<div class="skills-used">
    <strong>Key Tech:</strong> 
    <span class="badge badge-light">Semantic Segmentation</span>
    <span class="badge badge-light">Attention U-Net</span>
    <span class="badge badge-light">Medical Signal Processing</span>
    <span class="badge badge-light">SegFormer</span>
</div>
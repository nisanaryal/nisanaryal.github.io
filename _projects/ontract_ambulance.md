---
layout: page
title: Real-Time Ambulance Clinical Event Logging
description: Streamlining pre-hospital care by automating event detection and privacy-preserving data transmission from ambulances to emergency departments.
img: assets/img/ontact_detect.gif
importance: 2
category: Medical AI
---

<div class="project-metadata">
    <strong>Year:</strong> 2023 ~ 2026 <br>
    <strong>Workplace:</strong> <a href="https://www.mteg.co.kr/" target="_blank">MTEG</a>
</div>

---

### Project Overview
In emergency medicine, the "Golden Hour" is critical. This project focuses on automating the logging of medical interventions performed inside an ambulance. By detecting interactions between paramedics, patients, and medical equipment, the system generates real-time event logs that are transmitted to the receiving hospital, allowing doctors to prepare for the specific case details before the patient arrives.

### The "On-the-Move" Security Challenge
Similar to the ER setting, privacy was a non-negotiable requirement. However, this deployment faced stricter constraints:
1.  **Offline Deployment:** Due to secure vehicle network protocols, the de-identification model had to be trained and deployed in a strict **no-internet environment**.
2.  **Privacy First:** I implemented a localized face-blurring pipeline as a prerequisite to ensure that no raw, identifiable video data ever left the ambulance's local storage.

### Technical Implementation
The system utilizes a dual-engine approach to bridge the gap between raw video and clinical data:
* **Privacy Engine:** Real-time face detection and anonymization optimized for edge compute within the vehicle.
* **Interaction Engine:** Uses **Multi-Object Tracking (MOT)** to identify clinical actions (e.g., CPR, oxygen mask application, or IV starts) based on spatial relationships between personnel and specific medical kits.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/ontact_blur.gif" title="Mobile De-identification" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/ontact_detect.gif" title="Ambulance Event Tracking" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: Localized anonymization for mobile environments. Right: Automated detection of clinical interventions and personnel-equipment interaction.
</div>

### Technical Specifications
* **Architectures:** YOLO series and RT-DETR for high-speed inference on edge hardware.
* **Capabilities:** Interaction-based event triggering and automated timestamping for pre-hospital reports.
* **Security:** 100% on-device processing to comply with strict medical data sovereignty laws.

### Impact
* **Enhanced Preparedness:** Hospitals receive structured data on pre-hospital treatments, reducing the "information gap" during patient handovers.
* **Rapid Response Deployment:** Successfully transitioned from raw data collection to a deployed, secure model within a localized hospital network in just one week.

<div class="skills-used">
    <strong>Key Tech:</strong> 
    <span class="badge badge-light">Edge AI</span>
    <span class="badge badge-light">Privacy Preserving AI</span>
    <span class="badge badge-light">Action Recognition</span>
    <span class="badge badge-light">On-Premise Deployment</span>
</div>
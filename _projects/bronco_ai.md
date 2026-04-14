---
layout: page
title: "BronchoAI: Windows-Based Clinical Support System"
description: A high-performance desktop application for real-time bronchoscopic lung cancer detection, utilizing WebRTC for low-latency AI inference.
img: assets/img/bronco_ai.png
importance: 2
category: Medical AI
---

<div class="project-metadata">
    <strong>Year:</strong> 2025 <br>
    <strong>Role:</strong> Lead AI & System Architect <br>
    <strong>Architecture:</strong> Python Backend + Flutter Windows Frontend<br>
    <strong>Workplace:</strong> <a href="https://www.mteg.co.kr/" target="_blank">MTEG</a>

</div>

---

### Project Overview
Identifying malignancy during bronchoscopy requires high-precision visual analysis. I developed a comprehensive Windows desktop solution that integrates state-of-the-art computer vision with a professional clinical interface. The system detects lung anatomy and potential malignancies in real-time, providing surgeons with immediate diagnostic feedback and automated reporting tools.

### System Architecture & Communication
The core of this project is a high-performance bridge between deep learning models and the user interface:
* **Python AI Backend:** Handles the heavy lifting of video processing and model inference. It manages the detection of lung structures and malignant lesions while simultaneously handling high-speed video storage.
* **WebRTC Integration:** To ensure near-zero latency, I implemented a **WebRTC-based stream** to pipe the processed video from the Python backend directly to the Flutter application.
* **Flutter Windows Frontend:** A desktop application designed for the clinical environment, allowing doctors to trigger recordings, view live AI detections, and manage patient reports.

### The AI Engine: Comparative Benchmarking & Model Selection
To achieve a clinical-grade balance of sensitivity and specificity, I conducted an extensive benchmarking phase to identify the optimal architecture for the unique challenges of bronchoscopic imagery. The system was designed to leverage the strengths of various deep learning paradigms before settling on the most effective solution:

* **Model Benchmarking:** I evaluated several state-of-the-art architectures, including **ResNet** and **EfficientNet** for their robust feature extraction, alongside **Vision Transformers (ViT)** to assess their ability to capture global context and long-range dependencies in complex lung tissue.
* **Optimized Single-Model Deployment:** After rigorous testing against metrics for diagnostic accuracy and inference latency, I selected and deployed the best-performing model. This single-model approach ensures a streamlined pipeline, delivering high-sensitivity detection of malignant patterns while maintaining the real-time performance required for live clinical settings.
<div class="row justify-content-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include video.liquid path="assets/video/bronco_ai.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=true %}
    </div>
</div>
<div class="caption">
    The BronchoAI Desktop Interface: Real-time WebRTC streaming with AI-powered malignant lesion detection and interactive report editing.
</div>

### Technical Specifications
* **Core Models:** ResNet, EfficientNet-B4, Vision Transformer (ViT).
* **Communication:** WebRTC for real-time video, WebSocket/REST for control triggers.
* **Frontend:** Flutter for Windows (Desktop).
* **Backend:** Python (FastAPI/PyTorch) for inference and automated storage management.

### Impact
* **Low-Latency Performance:** WebRTC integration allowed for seamless real-time feedback during procedures, critical for surgical precision.
* **Integrated Workflow:** Consolidated the entire diagnostic chain—from live streaming and detection to storage and final report editing—into a single desktop workstation.

<div class="skills-used">
    <strong>Key Tech:</strong> 
    <span class="badge badge-light">WebRTC</span>
    <span class="badge badge-light">Flutter Windows</span>
    <span class="badge badge-light">Python Backend</span>
    <span class="badge badge-light">Vision Transformers (ViT)</span>
</div>
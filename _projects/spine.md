---
layout: page
title: Generative Spine Segmentation via Attention-XNet WGAN
description: High-fidelity vertebral segmentation using a modified X-Net generator within a Wasserstein GAN framework for robust spinal X-ray analysis.
img: assets/img/spine_1.png
importance: 2
category: Medical AI
---

<div class="project-metadata">
    <strong>Year:</strong> 2022 <br>
    <strong>Role:</strong> AI Research Engineer <br>
    <strong>Architecture:</strong> WGAN with Attention X-Net Generator<br>
    <strong>Workplace:</strong> <a href="https://www.mteg.co.kr/" target="_blank">MTEG</a>

</div>

---

### Project Overview
Spinal X-ray analysis requires extreme precision to identify vertebral boundaries for clinical diagnostics. This project addresses the challenge of segmentation in noisy or low-contrast X-ray images by employing a **Generative Adversarial Network (GAN)** approach.

By using a generative framework, the model learns to produce anatomically plausible masks that maintain structural consistency even in regions where traditional discriminative models might struggle with boundary ambiguity.

### Architecture: The Attention X-Net Generator
The core of this system is a modified **X-Net** (a nested U-Net variant) acting as the generator within a **Wasserstein GAN (WGAN)**.

* **Nested Feature Fusion (X-Net):** The generator uses redesigned skip connections to bridge the semantic gap between encoder and decoder features, capturing multi-scale spinal structures more effectively than a standard U-Net.
* **Attention Gates:** Integrated attention mechanisms allow the model to suppress irrelevant regions in the X-ray while focusing on the high-frequency details of the vertebral edges.
* **WGAN Stability:** Utilizing a Wasserstein loss with Gradient Penalty (WGAN-GP) ensured stable training and helped the generator converge toward producing realistic, sharp segmentation masks.

<div class="row justify-content-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/spine_1.png" title="Spine Segmentation Result 1" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="row justify-content-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/spine_2.png" title="Spine Segmentation Result 2" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="row justify-content-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/spine_3.png" title="Spine Segmentation Result 3" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    For each image: (Left) Original Spinal X-ray, (Middle) Predicted Segmentation Mask, (Right) Ground Truth Mask.
</div>

### Technical Specifications
* **Generator:** Modified X-Net with Attention Gates.
* **Discriminator:** PatchGAN-style critic focused on local texture and structural realism.
* **Loss Function:** Combined Adversarial (Wasserstein) loss and Pixel-wise (L1/Dice) loss to balance structural accuracy and generative realism.
* **Optimization:** Trained using Adam optimizer with weight clipping/gradient penalty to maintain WGAN stability.

### Impact
* **Anatomical Consistency:** The generative approach reduced "broken" segmentation artifacts common in pixel-wise classification models.
* **Enhanced Detail:** The attention-weighted nested connections successfully isolated vertebrae in images with high anatomical noise or overlapping structures.

<div class="skills-used">
    <strong>Key Tech:</strong> 
    <span class="badge badge-light">WGAN-GP</span>
    <span class="badge badge-light">X-Net / Nested U-Net</span>
    <span class="badge badge-light">Medical Image Segmentation</span>
    <span class="badge badge-light">Attention Mechanisms</span>
</div>
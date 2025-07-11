Image Sharpening using Knowledge Distillation

🎯 Objective
Develop a lightweight deep learning model to enhance image sharpness in real-time video conferencing scenarios, particularly addressing visual degradation due to low bandwidth or poor network conditions.

📚 Prerequisites
Machine Learning Concepts

Python Programming

Deep Learning (CNNs, Training/Evaluation)

Image Quality Metrics (SSIM, PSNR)

🧪 Approach
We use a Teacher–Student Knowledge Distillation framework:

Teacher Model:
Pre-trained SwinIR (Image Restoration Transformer) for high-fidelity outputs.

Student Model:
A lightweight CNN-based model designed to mimic the teacher’s performance with lower latency and computational cost.

⚙️ System Requirements
Feature	Specification
Target FPS	30–60+ FPS
Resolution	Supports 1920×1080 (Full HD)
Accuracy Metric	SSIM > 90%
Latency	Low (Real-time Inference)
Hardware	Edge/low-resource devices compatible

🧑‍💻 Training Setup
Dataset: High-resolution images (e.g., DIV2K, BSD500)

Data Simulation:

Downscale → Blur → Upscale (Bicubic/Bilinear)

Simulates compression artifacts from poor video connections.

Input: Simulated low-quality images

Ground Truth: Original high-resolution images

Loss Functions:

L1 Loss

Perceptual Loss

SSIM Loss

Distillation Loss (between teacher and student outputs)

🧪 Evaluation
Objective Metrics:

SSIM (Structural Similarity Index)

PSNR (Peak Signal-to-Noise Ratio)

Inference Time (in ms)

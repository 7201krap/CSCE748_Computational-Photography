# CSCE748_Computational-Photography

## 1. Introduction and Motivation

Image inpainting aims to fill in missing or corrupted regions of an image. While conventional methods rely on RGB information alone, we hypothesize that adding depth cues improves reconstruction, especially around object boundaries or occlusions. This project explores integrating a single-image depth map to enhance image reconstruction results.

## 2. Proposed Method

### 2.1 Baseline Models
- **CNN AutoEncoder: RGB Inpainting using RGB only**

### 2.2 Depth-Augmented Models
- **CNN AutoEncoder: RGB Inpainting using RGB + Depth with simple attention** 
- **CNN AutoEncoder: RGB Inpainting using RGB + Depth with multihead attention** 

We use NYU depth V2. We apply the same binary mask to both RGB and depth, ensuring the network “hallucinates” (i.e., forces the network to fill in) missing regions in the color

## 3. Experiments

- **Dataset & Masking**: Use a standard image dataset (e.g., NYU depth V2) with random masks.
- **Training**: Compare baseline (RGB-only) vs. depth-augmented approaches.
- **Evaluation Metrics**: PSNR, SSIM, LPIPS, and SSD to quantify reconstruction accuracy.

## 4. Expected Outcomes

We expect the depth-augmented models to produce higher PSNR and SSIM, and lower LPIPS and SSD, demonstrating improved visual fidelity over baseline methods. This could be particularly valuable in scenarios like autonomous driving or occluded object detection.

# Image Denoiser using U-Net integrated with CBAM

## Overview
This project presents a **multi-stage U-Net–based image restoration framework**
enhanced with **Convolutional Block Attention Modules (CBAM)** for real-world
RGB image denoising. The model progressively refines noisy images using residual
learning, enabling effective noise suppression while preserving fine details.

This work was carried out as a **Senior Design Project (SDP)** at
KLE Technological University, Hubballi.

## Architecture
The proposed model consists of:
- U-Net Stage 1 (coarse residual estimation)
- U-Net Stage 2 (fine residual refinement)
- Refinement block for final enhancement

Each stage integrates **CBAM** to apply channel-wise and spatial attention.

## Dataset
- Smartphone Image Denoising Dataset (SIDD)
- Real noisy–clean RGB image pairs
- 1600 images (train / validation / test)

## Training Details
- Framework: PyTorch
- Optimizer: AdamW
- Learning rate: 0.0002
- Batch size: 8
- Epochs: 50
- Loss: L1 Loss + 0.15 × SSIM Loss
- GPU: NVIDIA Tesla T4 (Google Colab)

## Results
| Metric | Value |
|------|------|
| PSNR | **33.63 dB** |
| SSIM | **0.87** |

The proposed model outperforms multiple existing denoising approaches on the
SIDD benchmark.

## Optimization
- Global unstructured L1 pruning
- Achieved 50% sparsity
- Minimal performance degradation after fine-tuning

## Repository Structure

image-denoiser-unet-cbam/
├── notebooks/
│ └── SDP2.ipynb
├── report/
│ └── Team3_CSAI_Report.pdf
├── README.md


## Sustainable Development Goal
Aligned with **SDG 9: Industry, Innovation, and Infrastructure**, particularly
Target 9.5 (enhancing scientific research and technological capabilities).

## Authors
- Abdul Rafay Attar
- Mohammed Sadiq Z Pattankudi
- Samarth Uppin
- Kashish Jewargi

## Institution
School of Computer Science and Engineering  
KLE Technological University, Hubballi

## License
Academic and research use only.

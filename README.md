# A Critical Evaluation of Diffusion Models: Exploring Their Limits in Open-World Anomaly Detection

This repository contains the full implementation of our exploratory project evaluating latent diffusion models, LoRA fine-tuning, and CLIP-based scoring for open-world industrial anomaly detection on the MVTec AD benchmark.

We investigate three modern reconstruction-based pipelines:

1. Stable Diffusion img2img reconstruction
2. DreamBooth-style LoRA fine-tuning on carpet textures
3. Reconstruction + hybrid anomaly scoring using CLIP + MSE

Our findings show that:
- Latent diffusion models fail at identity-preserving reconstruction due to the VAE bottleneck & generative sampling.
- Even fine-tuned LoRA models cannot reliably restore exact textures.
- CLIP-based scoring remains robust but is limited by reconstruction quality.

This repository includes full training scripts, reconstruction pipelines, anomaly scoring, evaluation metrics, and visualization utilities.

## Project Structure

codes/
├── diffusion_unet.ipynb
├── img2img.ipynb
└── finetune_lora.ipynb

report/
├── report.pdf
└── presentation.pdf

README.md
requirements.txt
.gitignore



## Installation
pip install -r requirements.txt

## Dataset
MvTec-AD dataset

## Contributors
Saksham Madan, Kushal Shrivastava, Arnav Raghuvanshi
Supervisor: Dr. Santwana Mukhopadhyay

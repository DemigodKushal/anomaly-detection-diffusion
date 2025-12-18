# Diffusion Models for Anomaly Detection (Extended Work)

This repository contains an **independent extension** of an earlier project on anomaly detection using diffusion-based reconstruction on the MVTec AD dataset.

The goal of this work is to understand how different diffusion training choices affect **reconstruction quality** and **anomaly localization**, and why large pretrained models often fail at identity-preserving reconstruction.

---

## Background

The original project experimented with:
- Stable Diffusion 1.5 img2img
- LoRA fine-tuning
- CLIP-based anomaly scoring

While these methods produced visually realistic images, they often changed textures and introduced artifacts, making reconstruction errors unreliable for anomaly detection.

The original report and slides are available in the `report/` folder.

---

## What I Have Tried So Far

- **Latent-space diffusion**
  - Initial experiments were done in latent space
  - Observed strong loss of texture and fine details
  - Reconstructions drifted away from the input image

- **Pixel-space diffusion**
  - Switched to training diffusion models directly in pixel space
  - Trained from scratch using only defect-free images
  - Produces more faithful and conservative reconstructions

- **v-prediction training**
  - Used instead of standard noise prediction
  - Gave more stable reconstructions across noise levels

- **Gaussian noise baseline**
  - Standard DDPM-style noise
  - Serves as the main working reference
  - Allows clearer residual maps for anomaly localization

- **Comparison with Stable Diffusion img2img**
  - Custom diffusion models preserve structure better
  - Fewer hallucinations
  - Residuals align better with anomalous regions

---

## Ongoing Work

- **Simplex noise experiments**
  - Inspired by AnoDDPM
  - Testing whether structured noise improves reconstruction
  - Still under investigation

- **Failure case analysis**
  - Over-smoothing
  - Loss of fine textures
  - Sensitivity to diffusion depth

---

## Status

This is an **experimental project**.  
Some ideas are still being tested and results may change.

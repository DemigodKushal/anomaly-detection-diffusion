# Extended Exploration of Diffusion Models for Open-World Anomaly Detection

This repository is an **independent continuation** of the original exploratory project on diffusion-based reconstruction for anomaly detection on the MVTec AD dataset.  
This fork adds new experiments, custom architectures, and deeper investigation into reconstruction failures and noise-process variations.

## Original Project (Context)
The original work evaluated:
1. Stable Diffusion img2img  
2. LoRA fine-tuning  
3. CLIP + MSE hybrid anomaly scoring  

and concluded that latent diffusion struggles with identity-preserving reconstruction.


**Currently I am working on testing and tinkering around an implementation of the novel idea of using simplex noise inplace of gaussian similar to what AnoDDPM does. **

You may find the original report and presentation in the report folder. 

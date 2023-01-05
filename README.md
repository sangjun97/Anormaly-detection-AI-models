# Anormaly-detection-AI-models
## 1. Introduction

## 2. Citation

## 3. Models
### 3-1. CNN

### 3-2. AutoEncoder

### 3-3. AnoGAN

### 3-4. AnoDDPM
For more details about AnoDDPM's technology, please refer to the AnoDDPM paper in the link.
> [Official Project](https://julianwyatt.co.uk/anoddpm) | [Paper](https://openaccess.thecvf.com/content/CVPR2022W/NTIRE/html/Wyatt_AnoDDPM_Anomaly_Detection_With_Denoising_Diffusion_Probabilistic_Models_Using_Simplex_CVPRW_2022_paper.html)

In this project, the files related to AnoDDPM are diffusion.py and UNet.py in the model folder and .py files in the core file.
```bash
├── model
│   ├── core
│       ├── evaluation.py
│       ├── helpers.py
│       ├── simplex.py
│       ├── solver.py
│       └── utils.py
│   ├── UNet.py
│   └── diffusion.py
├── dataloader.py
├── main.py
└── trainer.py
``` 

AnoDDPM is a model for Anomaly Detection based on Diffusion Model. It uses Simplex Noise, not Gaussian Mixture Noise, to compensate for the limitations that occur in the Anomaly Detection of DDPM, which is an existing Diffusion Model. Diffusion model using simplex noise has the advantage of generating a normal image well even for the low frequency region of an abnormal image.

In this project, the principle of AnoDDPM was also quoted to create an AnoDDPM model based on the diffusion model. Compared to existing generative models, the diffusion model shows superior performance in the generative domain. Therefore, it provides good performance image generation based on normal image features. Based on these images, it is compared with abnormal images, and if a certain threshold is exceeded, it is determined as an outlier.

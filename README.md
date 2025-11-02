# CIFAR-Denoise-Autoencoders
Denoising Autoencoders (Residual, CNN, UNet) on CIFAR-10 dataset

# CIFAR-Denoise-Autoencoders

Denoising Autoencoders (Residual, CNN, UNet) implemented in TensorFlow/Keras on the CIFAR-10 dataset.  
This project demonstrates image denoising using different autoencoder architectures.

## Features

- Residual Autoencoder
- CNN Autoencoder
- UNet Autoencoder
- Add Gaussian noise to CIFAR-10 images
- Visualize original, noisy, and denoised images

## Requirements

```bash
pip install -r requirements.txt

Usage

Run the main Python script:

python cifar_denoising_autoencoders.py


This will:

Load CIFAR-10 dataset

Add Gaussian noise

Train Residual Autoencoder

Plot original, noisy, and denoised images

Folder Structure
CIFAR-Denoise-Autoencoders/
│
├── cifar_denoising_autoencoders.py   # Main code
├── requirements.txt                  # Dependencies
├── README.md                         # Project info
├── .gitignore                        # Git ignore rules
└── results/                          # Optional output folder
CIFAR-10 Denoising Autoencoders

Denoising autoencoders implemented in TensorFlow/Keras to remove Gaussian noise from CIFAR-10 images.
This repository provides Residual, CNN, and UNet autoencoder architectures with visualization of noisy vs denoised images.

Features

Residual Autoencoder: Uses residual blocks for better feature learning.

CNN Autoencoder: Simple convolutional autoencoder for fast experimentation.

UNet Autoencoder: Encoder-decoder with skip connections for high-quality denoising.

Add Gaussian noise to CIFAR-10 dataset for training and testing.

Compare original, noisy, and denoised images side by side.

Optional saving of denoised images.

Dataset

CIFAR-10: 60,000 32x32 color images in 10 classes.

Loaded directly via tensorflow.keras.datasets.cifar10.

Images are normalized to [0,1] and Gaussian noise is added for denoising.

Requirements

Create a virtual environment (optional but recommended):

python -m venv venv
source venv/bin/activate      # Linux / Mac
venv\Scripts\activate         # Windows


Install dependencies:

pip install -r requirements.txt


requirements.txt example:

tensorflow>=2.10
numpy
matplotlib

Usage

Run the main script:

python cifar_denoising_autoencoders.py


This will:

Load and normalize CIFAR-10 images.

Add Gaussian noise.

Build and compile Residual, CNN, and UNet autoencoders.

Train the Residual Autoencoder (can extend to others).

Plot original, noisy, and denoised images.

Results

Original vs Noisy vs Denoised Images:
Images are displayed in rows: top = original, middle = noisy, bottom = denoised.

Optional: Save denoised images in results/ folder:

os.makedirs("results", exist_ok=True)
for i, img in enumerate(denoised):
    plt.imsave(f"results/denoised_{i}.png", img)

Project Structure
CIFAR-Denoise-Autoencoders/
│
├── cifar_denoising_autoencoders.py   # Main Python code
├── requirements.txt                  # Python dependencies
├── README.md                         # Project description
├── .gitignore                        # Ignore unnecessary files
└── results/                          # Folder to save denoised images

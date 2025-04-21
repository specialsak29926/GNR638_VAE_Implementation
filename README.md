
# Convolutional Variational Autoencoder (CVAE) UC Merced Dataset

## Project Overview
This project implements a Convolutional Variational Autoencoder (CVAE) using PyTorch to process and reconstruct images from the UC Merced Land Use dataset. The CVAE is trained to encode images into a low-dimensional latent space and then reconstruct them, capturing essential features while removing noise.

## Features
- Convolutional neural network architecture for encoding and decoding images
- Variational autoencoder implementation with KL divergence regularization
- Training pipeline with support for GPU acceleration
- Visualization of original and reconstructed images
- Model evaluation on validation and test datasets

## Model Architecture
The CVAE model consists of:
1. **Encoder**: A series of convolutional layers that reduce the image dimensions while increasing the channel count, followed by layers to compute the mean (μ) and log variance (logvar) of the latent space.
2. **Bottleneck**: A parameterized stochastic sampling from the encoded distribution.
3. **Decoder**: A series of transposed convolutional layers that reconstruct the original image from the latent representation.

## Loss Function
The model uses a combination of:
- Reconstruction loss (Mean Squared Error)
- KL divergence to regularize the latent space

## Dataset
The project uses the UC Merced Land Use dataset, which contains aerial imagery across different land use categories. The dataset should be organized with the following structure:
```
data/
  ├── train/
  ├── validation/
  ├── test/
```


## Training
The model is trained for 20 epochs with the following parameters:
- Batch size: 64
- Learning rate: 0.001
- KL weight: 0.8

## Results
The notebook includes visualization of original images alongside their reconstructions after training, demonstrating the model's ability to capture and reproduce essential features of the input images

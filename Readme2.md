# Convolutional Neural Network for MNIST Classification

## Introduction
This repository contains the implementation of a Convolutional Neural Network (CNN) for classifying handwritten digits from the MNIST dataset using PyTorch. The architecture of the CNN includes multiple convolutional layers, batch normalization, max-pooling, and dropout for regularization.

## Code Structure
- The neural network architecture is defined in the `Net` class, which inherits from `nn.Module`.
- Three convolutional blocks (`conv1`, `conv2`, `conv3`) are defined, each consisting of convolutional layers, ReLU activation, batch normalization, max-pooling, and dropout.
- The fully connected layer (`fc`) is responsible for the final classification.
- The `forward` method defines the forward pass of the network, including the application of each layer.
- The model summary is generated using the `torchsummary` library.

## Training
- The script includes functions for training (`train`) and testing (`test`) the model.
- Training is performed using the negative log-likelihood loss (`F.nll_loss`) and stochastic gradient descent (`optim.SGD`) as the optimizer.
- The training loop iterates over the MNIST training dataset, updating the model parameters to minimize the loss.
- The testing function evaluates the model on the MNIST test dataset and reports accuracy and average loss.

## Data Loading
- The MNIST dataset is loaded using the `torchvision` library, and transformations such as normalization and tensor conversion are applied.
- DataLoader objects are created for both the training and test datasets.

## Execution
- The script can be executed to train and test the model on the MNIST dataset.
- Model training and testing progress is displayed using the `tqdm` library.

## Usage
1. Install the required libraries: `torch`, `torchvision`, `torchsummary`, `tqdm`.
2. Execute the script to train and test the CNN on the MNIST dataset.

## Dependencies
- Python 3.x
- PyTorch
- torchvision
- torchsummary
- tqdm

Feel free to modify the hyperparameters, architecture, or other aspects of the code to experiment and improve the model's performance.
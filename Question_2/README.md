# CIFAR-100 Image Classification with Custom CNN and Standard Architectures

## Project Overview

This repository contains the implementation of a custom CNN architecture for CIFAR-100 image classification and comparisons with standard deep learning architectures (ResNet-50, VGG-19, DenseNet-121, and EfficientNet-B0).

## Files and Directory Structure

- `Assignment1_Question2.ipynb`: Jupyter notebook containing all implementation code
  - [Open in Google Colab](https://colab.research.google.com/drive/1TBx4d4qjJXPEPVMoSQTaHqX7xABTKLAa?usp=sharing) 

- `docs/`: Report documents
  - `Custom_CNN_Architecture.md`: Details of the custom CNN design
  - `Implementation_Details.md`: Training configuration and preprocessing information
  - `Model_Comparison.md`: Comparative analysis of all models

- Generated output files:
  - `*_training_history.png`: Training and validation loss/accuracy plots
  - `*_filters.png`: Visualization of convolutional filters
  - `*_confusion_matrix.png`: Confusion matrices for all models
  - `model_comparison.png`: Comparative bar chart of model performance
  - `model_comparison.csv`: Tabular results data

## Requirements

All requirements are automatically installed in the Colab notebook. If running locally, you'll need:
- Python 3.7+
- PyTorch 1.7+
- torchvision
- NumPy
- Matplotlib
- scikit-learn
- pandas
- seaborn

## Usage

### Option 1: Google Colab (Recommended)
1. Click the "Open in Google Colab" link above
2. Run all cells in the notebook

### Option 2: Local Execution
1. Download the `Assignment1_Question2.ipynb` notebook
2. Run using Jupyter:
```bash
jupyter notebook Assignment1_Question2.ipynb
```

Both options will:
- Download the CIFAR-100 dataset if not present
- Train the custom CNN model
- Train all standard models (ResNet-50, VGG-19, DenseNet-121, EfficientNet-B0)
- Generate visualizations
- Compare model performance

## Note on Model Files

The trained model files (*.pth) are excluded from this repository due to their large size. The notebook will automatically generate these files when run. When using Google Colab, you may want to save the models to your Google Drive for persistence.

## Key Results

- ResNet-50 achieved the highest accuracy (63.11%)
- Our custom CNN ranked second (55.60%)
- DenseNet-121 achieved 52.89%
- EfficientNet-B0 achieved 33.42%
- VGG-19 struggled to train effectively (2.41%)

## Implementation Details

The custom CNN architecture features:
- 6 convolutional layers arranged in 3 blocks
- Batch normalization and dropout for regularization
- Global average pooling
- Data augmentation with random crops, flips, and color jitter

Training used:
- Adam optimizer with learning rate 0.001
- Cross-entropy loss
- Learning rate scheduling and early stopping

For detailed information, see the report documents in the `docs/` directory or review the notebook comments.
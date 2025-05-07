# Implementation Details

## Hyperparameters and Training Configuration

### Optimizer
- **Adam optimizer**: Selected for its adaptive learning rate capabilities, momentum, and efficiency in navigating noisy gradients
- **Learning rate**: 0.001 (1e-3)
- **Weight decay**: 1e-4 for L2 regularization to prevent overfitting

### Loss Function
- **Cross-Entropy Loss**: Appropriate for multi-class classification problems like CIFAR-100

### Learning Rate Scheduling
- **ReduceLROnPlateau**: Reduces learning rate when validation metrics plateau
- **Factor**: 0.5 (halves the learning rate)
- **Patience**: 5 epochs
- **Mode**: 'max' (monitoring validation accuracy)

### Batch Size
- **128 samples per batch**: Balances training speed and memory requirements while providing stable gradient estimates

### Training Duration
- **Maximum epochs**: 10
- **Early stopping patience**: 10 epochs
- **Best model saving**: Based on validation accuracy

## Data Preprocessing and Augmentation

### Normalization
- **Mean**: (0.5071, 0.4867, 0.4408)
- **Standard deviation**: (0.2675, 0.2565, 0.2761)
- These values are the channel-wise means and standard deviations of the CIFAR-100 dataset

### Training Data Augmentation
1. **Random Crop**: 32×32 with padding of 4 pixels
2. **Random Horizontal Flip**: 50% probability
3. **Color Jitter**: Brightness and contrast variations of ±20%
4. **To Tensor**: Conversion to PyTorch tensors
5. **Normalization**: Using channel-specific means and standard deviations

### Testing Data Transformation
1. **To Tensor**: Conversion to PyTorch tensors
2. **Normalization**: Same normalization as training data

## Training Process

- **Device**: CUDA GPU (when available), falling back to CPU
- **Reproducibility**: Fixed random seed (42) for consistent results
- **Batch Processing**: 2 worker processes for data loading
- **Validation Strategy**: Test set used for validation after each epoch

### Early Stopping Implementation
- Monitors validation accuracy
- Saves best model weights
- Stops training when no improvement is seen for the specified patience period

## Filter Visualization Mechanism

- Storage of initial filter weights when training begins
- Capture of final weights after training completes
- Visualization before and after training to observe learned patterns
- Normalization of filter values for clear visualization
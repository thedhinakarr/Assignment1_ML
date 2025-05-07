# Model Comparison

## Performance Metrics Comparison

| Model | Accuracy | Precision | Recall | F1-Score | TP | FP | FN |
|-------|----------|-----------|--------|----------|------|------|------|
| CustomCNN | 0.5560 | 0.5643 | 0.5560 | 0.5524 | 5560 | 4440 | 4440 |
| ResNet-50 | 0.6311 | 0.6526 | 0.6311 | 0.6269 | 6311 | 3689 | 3689 |
| VGG-19 | 0.0241 | 0.0042 | 0.0241 | 0.0058 | 241 | 9759 | 9759 |
| DenseNet-121 | 0.5289 | 0.5304 | 0.5289 | 0.5201 | 5289 | 4711 | 4711 |
| EfficientNet-B0 | 0.3342 | 0.3331 | 0.3342 | 0.3212 | 3342 | 6658 | 6658 |

## Analysis of Results

### Model Performance Ranking
1. **ResNet-50** (63.11% accuracy)
2. **CustomCNN** (55.60% accuracy)
3. **DenseNet-121** (52.89% accuracy) 
4. **EfficientNet-B0** (33.42% accuracy)
5. **VGG-19** (2.41% accuracy)

### Performance Analysis

#### ResNet-50
- Top performer with 63.11% accuracy
- Skip connections (residual blocks) likely contribute to its superior performance by addressing the vanishing gradient problem
- Strong precision (65.26%) indicates reliable positive predictions
- Well-balanced precision and recall suggest good performance across classes

#### CustomCNN
- Second-best performer with 55.60% accuracy
- Competitive performance despite simpler architecture compared to pre-trained models
- Well-balanced metrics indicate consistent performance across classes
- Only 7.51% behind ResNet-50, demonstrating the effectiveness of the custom design

#### DenseNet-121
- Third place with 52.89% accuracy
- Dense connections did not outperform ResNet architecture for this specific task
- Slightly lower than the custom model despite greater complexity

#### EfficientNet-B0
- Fourth place with only 33.42% accuracy
- Designed for efficiency but struggled with the complexity of CIFAR-100
- Significantly underperformed compared to the top three models

#### VGG-19
- Failed to train properly, achieving only 2.41% accuracy
- Extremely low precision (0.42%) indicates almost random positive predictions
- Deep architecture likely suffered from optimization issues given the limited training time
- May require more epochs or custom learning rate scheduling to train effectively

### Key Observations

1. **Architecture Importance**: Skip connections (ResNet) appear to be crucial for deep network performance on CIFAR-100.

2. **CustomCNN Effectiveness**: The custom architecture achieved competitive performance despite being simpler than the pre-trained models, demonstrating that well-designed moderate-sized networks can be effective for this task.

3. **Training Challenges**: VGG-19's poor performance highlights the difficulties in training very deep networks without skip connections, especially with limited epochs.

4. **Model Complexity vs. Performance**: More complex models do not always yield better results, as shown by CustomCNN outperforming DenseNet-121 and EfficientNet-B0.

## Training Curves Analysis

All successful models showed consistent improvements in both training and validation metrics throughout the training process. The custom model's validation metrics consistently exceeded training metrics, indicating effective regularization and no overfitting.

## Filter Visualization Insights

The convolutional filters in the first layer evolved from random initializations to structured patterns during training. The custom model developed filters sensitive to edges, textures, and color gradients, which are fundamental for image recognition tasks.

This comparison demonstrates that while state-of-the-art architectures like ResNet-50 provide superior performance, a well-designed custom CNN can achieve competitive results while potentially offering advantages in interpretability and computational efficiency.
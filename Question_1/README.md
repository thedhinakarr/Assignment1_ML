# Gradient Descent Implementation for Function Minimization

## Assignment 1 - Question 1

This repository contains the implementation of gradient descent optimization to find the minimum of the function:

```
f(x, y) = x² + y² + x(y + 2) + cos(3x)
```

## Google Colab Notebook

You can run this implementation directly in Google Colab using the following link:
[Open in Google Colab](https://colab.research.google.com/drive/1nzYDL7j-Z5piEIQUOd3qWdp1v6x5vM1_?usp=sharing)


## Implementation Overview

The implementation includes:

1. **Analytical Derivatives**:
   - ∂f/∂x = 2x + (y + 2) - 3sin(3x)
   - ∂f/∂y = 2y + x

2. **Optimization Algorithms**:
   - Standard Gradient Descent with multiple learning rates (0.01, 0.05, 0.1)
   - Gradient Descent with Momentum (momentum coefficient = 0.9)

3. **Visualizations**:
   - 3D surface plot of the function
   - Contour plots with gradient descent paths
   - Function value and gradient norm convergence plots
   - Gradient vector field visualization
   - Comparative analysis of different methods

## Key Results

- The global minimum is located at approximately x = -1.08, y = 0.54
- The minimum function value is approximately -2.28071
- Gradient descent with momentum achieves a 62% reduction in required iterations compared to standard gradient descent (235 vs. 618 iterations)
- Higher learning rates provide faster convergence but may introduce oscillatory behavior
- The function's periodic component (cos(3x)) creates local ripples in the gradient field but does not prevent convergence to the global minimum

## How to Run

### Option 1: Google Colab (Recommended)
1. Open the notebook using the Google Colab link provided above
2. Select "Runtime" > "Run all" to execute all cells
3. No installation required - everything runs in the cloud

### Option 2: Local Execution
1. Clone this repository
2. Open the Jupyter notebook `Assignment1_Question1_GradientDescent.ipynb`
3. Run all cells sequentially to reproduce the results

The notebook is divided into the following sections:
- Function and gradient definitions
- Standard gradient descent implementation
- Momentum-based gradient descent implementation
- Visualization functions
- Results analysis and comparison

## Parameters

The following parameters can be adjusted in the notebook:
- `learning_rate`: Controls step size (default values: 0.01, 0.05, 0.1)
- `momentum`: Controls the momentum effect (default: 0.9)
- `initial_point`: Starting position for optimization (default: [2.0, 2.0])
- `max_iterations`: Maximum number of iterations (default: 1000)
- `tolerance`: Convergence criterion threshold (default: 1e-6)

## Visualizations

### Gradient Descent Paths
Shows the function landscape as both a 3D surface and contour plot with paths taken by different gradient descent variants with various learning rates.

### Convergence Analysis
Tracks how function value and gradient norm change during the optimization process, providing insights into convergence behavior.

### Gradient Vector Field
Displays the direction of steepest descent at different points in the function domain, revealing how the optimization process navigates the landscape.

### GD vs. Momentum Comparison
Directly compares the performance of standard gradient descent and momentum-based gradient descent, demonstrating the efficiency gain from using momentum.

### Minimum Point Analysis
Provides a zoomed-in view of the region around the minimum, confirming the quadratic nature of the function near its minimum point.

## Dependencies

This implementation requires the following Python libraries:
- NumPy: For numerical computations
- Matplotlib: For creating visualizations
- Mpl_toolkits.mplot3d: For 3D plotting

All dependencies are pre-installed in Google Colab.

## Technical Report

The included IEEE-formatted technical report (`Deep_learning_Question_1_Report.pdf`) provides a comprehensive analysis of the implementation and results. It includes:

- Mathematical derivation of the gradient
- Detailed explanation of the optimization algorithms
- Analysis of learning rate effects
- Comparison between standard GD and momentum-based GD
- Visualizations and their interpretation
- Conclusions and potential future work

## Conclusion

This implementation demonstrates how gradient descent effectively finds the minimum of a non-convex function. The momentum-based variant provides substantial performance improvements, reducing the required iterations by 62%. The comprehensive visualizations offer valuable insights into the optimization landscape and the behavior of different gradient descent variants.

## Author

Dhinakar R
Blekinge Institute of Technology
Karlskrona, Sweden
dhra24@student.bth.se

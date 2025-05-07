# Visualization Guide

This document explains the visualizations created for the gradient descent implementation.

## 3D Surface Plot

![3D Function Surface with Gradient Descent Paths](../Plots/gradient_descent_surface_contour.png)

**Purpose**: Shows the 3D landscape of the function f(x, y) = x² + y² + x(y + 2) + cos(3x)

**Features**:
- **Surface coloring**: Represents function values (blue = low, yellow = high)
- **Colored paths**: Shows gradient descent trajectories for different learning rates
- **Perspective view**: Reveals the bowl-shaped quadratic component with ripples from the cosine term

**Interpretation**:
- The function has a global minimum in a valley with surrounding ripples
- All paths eventually converge to the same minimum
- Higher learning rates take larger steps, visible by the spacing between points

## Contour Plot

![Contour Plot with Gradient Descent Paths](../Plots/gradient_descent_surface_contour.png)

**Purpose**: Provides a top-down view of the function landscape

**Features**:
- **Contour lines**: Level curves of equal function value
- **Path trajectories**: Shows how the algorithms navigate the landscape
- **Color gradient**: Indicates function values (blue = low, yellow = high)

**Interpretation**:
- Closely spaced contour lines indicate steep gradients
- Paths always move perpendicular to contour lines (direction of steepest descent)
- The ripples from the cosine term create interesting contour patterns

## Convergence Plots

![Convergence of Function Value and Gradient Norm](../Plots/gradient_descent_convergence.png)

**Purpose**: Tracks convergence progress for different learning rates

**Left plot features**:
- **Y-axis**: Function value during optimization
- **X-axis**: Iteration number
- **Multiple curves**: Compare different learning rates

**Right plot features**:
- **Y-axis**: Logarithmic scale of gradient norm
- **X-axis**: Iteration number
- **Exponential decay**: Shows how quickly gradient approaches zero

**Interpretation**:
- Steeper descent curves indicate faster convergence
- The small learning rate (0.01) shows a plateau around iterations 50-125
- The gradient norm plot confirms exponential convergence rates

## Gradient Vector Field

![Gradient Vector Field with Descent Path](../Plots/gradient_vector_field.png)

**Purpose**: Visualizes the direction of steepest descent across the function domain

**Features**:
- **Red arrows**: Normalized negative gradient directions
- **Contour background**: Function level curves
- **Blue path**: Example gradient descent trajectory
- **Green/red points**: Start and end positions

**Interpretation**:
- Arrows always point perpendicular to contour lines
- The algorithm follows the direction indicated by the arrows
- Areas with complex arrow patterns indicate regions with changing gradient directions

## Methods Comparison

![Comparison of Gradient Descent Methods](../Plots/gradient_descent_comparison.png)

**Purpose**: Compares standard gradient descent with momentum-enhanced version

**Left plot features**:
- **Contour background**: Function landscape
- **Blue path**: Standard gradient descent trajectory
- **Red path**: Momentum-enhanced trajectory

**Right plot features**:
- **Y-axis**: Function value
- **X-axis**: Iteration number
- **Convergence rates**: Shows how quickly each method approaches minimum

**Interpretation**:
- Momentum takes a more direct path to the minimum
- Standard GD requires 618 iterations vs. 235 for momentum (62% reduction)
- Momentum shows characteristic oscillation but dampens quickly

## Minimum Point Visualization

![Zoomed-in View of the Minimum Point](../Plots/minimum_point_zoom.png)

**Purpose**: Provides detailed view of the region around the minimum

**Features**:
- **Fine contour lines**: Detailed level curves near minimum
- **Red dot**: Location of the minimum
- **Tight zoom**: Focused on a small region around the minimum point

**Interpretation**:
- Elliptical contour lines confirm the quadratic nature near the minimum
- The minimum occurs at approximately (-1.08, 0.54)
- Function value at minimum is approximately -2.28071

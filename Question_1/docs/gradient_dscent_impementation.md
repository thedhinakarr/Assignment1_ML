# Gradient Descent Implementation

## Mathematical Foundation

### Derivatives
For the function f(x, y) = x² + y² + x(y + 2) + cos(3x):

- Partial derivative with respect to x: ∂f/∂x = 2x + (y + 2) - 3sin(3x)
- Partial derivative with respect to y: ∂f/∂y = 2y + x

### Gradient Descent Algorithms

#### Standard Gradient Descent
The algorithm iteratively updates the position (x, y) using:
(x, y)ᵗ⁺¹ = (x, y)ᵗ - η∇f(x, y)ᵗ

where:
- (x, y)ᵗ is the position at iteration t
- η is the learning rate
- ∇f(x, y)ᵗ is the gradient at iteration t

#### Gradient Descent with Momentum
Enhanced algorithm that incorporates velocity:
vᵗ⁺¹ = μvᵗ - η∇f(x, y)ᵗ
(x, y)ᵗ⁺¹ = (x, y)ᵗ + vᵗ⁺¹

where:
- vᵗ is the velocity at iteration t
- μ is the momentum coefficient (set to 0.9)

## Implementation Details

The implementation in the Jupyter notebook includes:
1. Function and gradient definitions
2. Standard gradient descent with multiple learning rates (0.01, 0.05, 0.1)
3. Enhanced gradient descent with momentum
4. Comprehensive visualizations:
   - 3D surface plot with descent paths
   - Contour plot with gradient descent trajectories
   - Convergence plots for function value and gradient norm
   - Gradient vector field visualization
   - Comparison between standard GD and momentum GD

## Results

### Minimum Found
- Coordinates: x ≈ -1.08, y ≈ 0.54
- Function value: f(x, y) ≈ -2.28071

### Learning Rate Comparison
| Learning Rate | Iterations | Convergence Behavior |
|---------------|------------|----------------------|
| 0.01 | 618 | Slow but very stable |
| 0.05 | ~150 | Good balance of speed and stability |
| 0.1 | ~75 | Fast but slight oscillation risk |

### Algorithm Comparison
| Algorithm | Iterations | Advantage | Disadvantage |
|-----------|------------|-----------|--------------|
| Standard GD | 618 | Simple implementation | Slower convergence |
| GD with Momentum | 235 | 62% faster convergence | Slight implementation complexity |

## Visualization Analysis

1. The 3D surface and contour plots reveal how the function's periodic component creates ripples along the x-axis
2. The vector field demonstrates how gradient directions guide the optimization process
3. The convergence plots illustrate exponential convergence rates for different methods
4. The zoomed-in view confirms the elliptical nature of level sets near the minimum

## Conclusion

Both standard gradient descent and gradient descent with momentum successfully find the minimum of the function. The enhanced version with momentum demonstrates significant performance improvement, requiring 62% fewer iterations to converge to the same minimum value.

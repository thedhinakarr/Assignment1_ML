# Mathematical Derivation

## Function Definition
f(x, y) = x² + y² + x(y + 2) + cos(3x)

## Derivative with Respect to x
To find ∂f/∂x, we apply the derivative rules to each term:

1. Derivative of x²: 2x
2. Derivative of y² with respect to x: 0
3. Derivative of x(y + 2): (y + 2)
4. Derivative of cos(3x): -3sin(3x)

Adding these terms:
∂f/∂x = 2x + (y + 2) - 3sin(3x)

## Derivative with Respect to y
To find ∂f/∂y, we apply the derivative rules to each term:

1. Derivative of x² with respect to y: 0
2. Derivative of y²: 2y
3. Derivative of x(y + 2): x
4. Derivative of cos(3x) with respect to y: 0

Adding these terms:
∂f/∂y = 2y + x

## Gradient Vector
The gradient vector is:
∇f(x, y) = [∂f/∂x, ∂f/∂y] = [2x + (y + 2) - 3sin(3x), 2y + x]

## Critical Points Analysis
At critical points, both partial derivatives equal zero:

2x + (y + 2) - 3sin(3x) = 0
2y + x = 0

From the second equation:
y = -x/2

Substituting into the first equation:
2x + (-x/2 + 2) - 3sin(3x) = 0
2x - x/2 + 2 - 3sin(3x) = 0
3x/2 + 2 - 3sin(3x) = 0
3x/2 - 3sin(3x) = -2
x/2 - sin(3x) = -2/3
x - 2sin(3x) = -4/3

This transcendental equation can be solved numerically, yielding the critical point at approximately:
x ≈ -1.08, y ≈ 0.54

## Hessian Matrix Analysis
The Hessian matrix H contains the second partial derivatives:

H(x, y) = [∂²f/∂x², ∂²f/∂x∂y; ∂²f/∂y∂x, ∂²f/∂y²]

Computing each element:
∂²f/∂x² = 2 - 9cos(3x)
∂²f/∂x∂y = ∂²f/∂y∂x = 1
∂²f/∂y² = 2

At the critical point (x ≈ -1.08, y ≈ 0.54):
∂²f/∂x² ≈ 2 - 9cos(3 × (-1.08)) ≈ 2 - 9cos(-3.24) ≈ 2 - 9(-0.99) ≈ 10.91
∂²f/∂y² = 2

The Hessian matrix is:
H(-1.08, 0.54) ≈ [10.91, 1; 1, 2]

The eigenvalues are both positive (approximately 11.01 and 1.9), confirming this critical point is a local minimum.

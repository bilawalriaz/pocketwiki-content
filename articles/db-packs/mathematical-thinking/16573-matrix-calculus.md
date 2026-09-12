# Matrix calculus

Matrix calculus is a notation that collects the many partial derivatives of multivariable functions into vectors and matrices, so that a scalar-by-vector or vector-by-matrix derivative can be written as a single object and manipulated with matrix algebra. The notation is standard in statistics, engineering, and machine learning, while physicists usually prefer tensor index notation with Einstein summation, which scales better to rank-3 and higher objects.

## Scope

Because the independent and dependent variables can each be a scalar, a vector, or a matrix, there are nine possible combinations. The six that fit cleanly into a 2-D matrix are the ones treated by the notation: scalar-by-scalar, scalar-by-vector, vector-by-scalar, vector-by-vector, scalar-by-matrix, and matrix-by-scalar. The remaining three (vector-by-matrix, matrix-by-vector, matrix-by-matrix) are naturally tensors of rank higher than 2.

The notation distinguishes objects by typeface: bold capital (**A**, **X**) for $m \times n$ matrices, bold lowercase (**a**, **x**) for column vectors in $M(n,1)$, and italic lowercase for scalars. All functions are assumed $C^1$.

## Vector derivatives

The derivative of a column vector $\mathbf{y} = [y_1, \ldots, y_m]^\top$ by a scalar $x$ stacks the components into a column:

$$\frac{d\mathbf{y}}{dx} = \left[\frac{dy_1}{dx}, \frac{dy_2}{dx}, \ldots, \frac{dy_m}{dx}\right]^\top.$$

This is the **tangent vector**; velocity is the tangent of position, acceleration the tangent of velocity.

The derivative of a scalar $y$ by a vector $\mathbf{x} = [x_1, \ldots, x_n]^\top$ produces a row vector of partials:

$$\frac{\partial y}{\partial \mathbf{x}} = \left[\frac{\partial y}{\partial x_1}, \ldots, \frac{\partial y}{\partial x_n}\right],$$

whose transpose is the **gradient** $\nabla f$. The directional derivative of $f$ in direction $\mathbf{u}$ is $\nabla_u f = (\partial f/\partial \mathbf{x})\,\mathbf{u}$. In physics, the electric field is $-\nabla$ of the electric potential.

The derivative of a vector $\mathbf{y}$ by a vector $\mathbf{x}$ is the $m \times n$ **Jacobian matrix** of partials $\partial y_i/\partial x_j$. It is also called the pushforward or differential, and satisfies $d\mathbf{f} = (\partial \mathbf{f}/\partial \mathbf{v})\,d\mathbf{v}$.

## Matrix derivatives

The derivative of an $m \times n$ matrix $\mathbf{Y}$ by a scalar $x$ is the **tangent matrix** of elementwise partials. The derivative of a scalar $y$ by a $p \times q$ matrix $\mathbf{X}$ is the **gradient matrix** $\partial y/\partial \mathbf{X}$ of partials with respect to each $x_{ij}$, central to minimization problems in estimation theory; the Kalman filter derivation depends on it. The directional derivative of $f(\mathbf{X})$ in the direction of $\mathbf{Y}$ is $\nabla_{\mathbf{Y}} f = \mathrm{tr}\!\left((\partial f/\partial \mathbf{X})\mathbf{Y}\right)$.

## The two layout conventions

The same derivative $\partial \mathbf{y}/\partial \mathbf{x}$ can be laid out as either an $m \times n$ or an $n \times m$ matrix, which splits the field:

- **Numerator layout** (the "Jacobian formulation"): rows follow the numerator $\mathbf{y}$, columns the denominator $\mathbf{x}$. The gradient $\partial y/\partial \mathbf{x}$ is a *row* vector.
- **Denominator layout** (the "Hessian formulation"): rows follow $\mathbf{x}$, columns $\mathbf{y}$. The gradient is a *column* vector.

Switching between the two transposes every result. Many authors mix layouts across different derivative types (for instance, denominator layout for gradients but numerator for Jacobian), and no single convention has emerged as standard. Serious errors arise when formulas from different conventions are combined without checking; the safest practice is to identify the layout used in each source and maintain it consistently, transposing at the end if a column-vector answer is required.

## Identities

The sum rule applies universally and the product rule holds provided the order of matrix products is preserved (matrix multiplication is not commutative). The chain rule applies to vector derivatives but fails in scalar-by-matrix form; there, one works in differential form and converts back.

Differential form is often easier: $d(\mathbf{XY}) = (d\mathbf{X})\mathbf{Y} + \mathbf{X}(d\mathbf{Y})$, $d(\mathbf{X}^{-1}) = -\mathbf{X}^{-1}(d\mathbf{X})\mathbf{X}^{-1}$, $d\,\mathrm{tr}(\mathbf{X}) = \mathrm{tr}(d\mathbf{X})$, $d\ln|\mathbf{X}| = \mathrm{tr}(\mathbf{X}^{-1}d\mathbf{X})$, and $d\,|\mathbf{X}| = |\mathbf{X}|\,\mathrm{tr}(\mathbf{X}^{-1}d\mathbf{X})$. Because $\mathrm{tr}$ permits cyclic permutation, $\mathrm{tr}(ABCD) = \mathrm{tr}(BCDA) = \mathrm{tr}(CDAB) = \mathrm{tr}(DABC)$, which is the key tool for working with trace derivatives.

A worked example: differentiating $\mathrm{tr}(\mathbf{AXBX}^\top\mathbf{C})$ with respect to $\mathbf{X}$ uses the trace-cyclic property repeatedly to extract $d\mathbf{X}$, giving

$$\frac{\partial\,\mathrm{tr}(\mathbf{AXBX}^\top\mathbf{C})}{\partial\mathbf{X}} = \mathbf{B}^\top\mathbf{X}^\top\mathbf{A}^\top\mathbf{C}^\top + \mathbf{BX}^\top\mathbf{CA} \quad \text{(numerator layout)},$$

with the denominator-layout result being its transpose.

Other useful identities in numerator layout: $\partial\,\mathrm{tr}(\mathbf{AX})/\partial\mathbf{X} = \mathbf{A}$, $\partial\,\mathrm{tr}(\mathbf{X}^\top\mathbf{AX})/\partial\mathbf{X} = \mathbf{X}^\top(\mathbf{A} + \mathbf{A}^\top)$, and $\partial\,\mathrm{tr}(\mathbf{X}^n)/\partial\mathbf{X} = n\mathbf{X}^{n-1}$. For vectors, $\partial\,\mathbf{x}^\top\mathbf{x}/\partial\mathbf{x} = 2\mathbf{x}^\top$ and $\partial\,\mathbf{x}^\top\mathbf{Ax}/\partial\mathbf{x} = \mathbf{x}^\top(\mathbf{A}+\mathbf{A}^\top)$, collapsing to $2\mathbf{Ax}$ when $\mathbf{A}$ is symmetric.

## Applications

Matrix calculus underlies the derivation of optimal stochastic estimators including the Kalman filter, Wiener filter, expectation-maximization for Gaussian mixtures, and gradient descent. It is the standard tool in regression analysis for deriving the ordinary least-squares formula with multiple explanatory variables, and in the statistical analysis of multivariate normal and other elliptical distributions, random matrices, and local sensitivity diagnostics. The Fréchet derivative agrees with the matrix derivative up to notation whenever both exist, so the same rules cover the functional-analysis setting.

Source: adapted from "Matrix calculus" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Matrix_calculus

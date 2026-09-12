# Matrix difference equation

A matrix difference equation is a difference equation in which a vector of variables at one time step is related to its own value at earlier time steps through matrices. The order is the largest time gap between any two values of the vector in the equation. First-order equations are the most common.

A representative second-order homogeneous example is:

$$\mathbf{x}_t = \mathbf{A}\mathbf{x}_{t-1} + \mathbf{B}\mathbf{x}_{t-2}$$

with $\mathbf{x}$ an $n \times 1$ column vector and $\mathbf{A}$, $\mathbf{B}$ both $n \times n$. The same relation also appears written forward as $\mathbf{x}_{t+2} = \mathbf{A}\mathbf{x}_{t+1} + \mathbf{B}\mathbf{x}_t$.

## Nonhomogeneous form and the steady state

A nonhomogeneous first-order equation adds a constant vector:

$$\mathbf{x}_t = \mathbf{A}\mathbf{x}_{t-1} + \mathbf{b}$$

A steady state $\mathbf{x}^*$ is a value the system would not leave once reached. Setting $\mathbf{x}_t = \mathbf{x}_{t-1} = \mathbf{x}^*$ and solving gives:

$$\mathbf{x}^* = [\mathbf{I} - \mathbf{A}]^{-1}\mathbf{b}$$

which requires $[\mathbf{I} - \mathbf{A}]$ to be invertible. Substituting back yields the deviation form:

$$[\mathbf{x}_t - \mathbf{x}^*] = \mathbf{A}[\mathbf{x}_{t-1} - \mathbf{x}^*]$$

so any nonhomogeneous first-order system can be analysed as a homogeneous one in deviations from $\mathbf{x}^*$.

## Solution and stability of the first-order case

Take the homogeneous form $\mathbf{y}_t = \mathbf{A}\mathbf{y}_{t-1}$ with initial vector $\mathbf{y}_0$. Iterating gives $\mathbf{y}_1 = \mathbf{A}\mathbf{y}_0$, $\mathbf{y}_2 = \mathbf{A}^2\mathbf{y}_0$, $\mathbf{y}_3 = \mathbf{A}^3\mathbf{y}_0$, and by induction:

$$\mathbf{y}_t = \mathbf{A}^t \mathbf{y}_0$$

If $\mathbf{A}$ is diagonalizable with distinct eigenvalues, writing $\mathbf{A} = \mathbf{P}\mathbf{D}\mathbf{P}^{-1}$ where $\mathbf{P}$ collects the eigenvectors and $\mathbf{D}$ is the diagonal matrix of eigenvalues gives:

$$\mathbf{y}_t = \mathbf{P}\mathbf{D}^t\mathbf{P}^{-1}\mathbf{y}_0$$

Stability follows directly: $\mathbf{x}_t$ converges to $\mathbf{x}^*$ if and only if every eigenvalue of $\mathbf{A}$ has absolute value less than 1 (spectral radius below 1). All eigenvalues inside the unit disk force $\mathbf{A}^t$ toward the zero matrix; any eigenvalue outside causes divergence.

## From a vector to a single scalar recurrence

Each component of an $n$-dimensional first-order system satisfies an $n$th-order scalar difference equation. The vector solution shows that $y_{1,t}$ depends on all $n$ eigenvalues of $\mathbf{A}$, so $y_1$ by itself must evolve by:

$$y_{1,t} = a_1 y_{1,t-1} + a_2 y_{1,t-2} + \cdots + a_n y_{1,t-n}$$

The coefficients $a_i$ come from the characteristic equation of $\mathbf{A}$:

$$\lambda^n - a_1 \lambda^{n-1} - a_2 \lambda^{n-2} - \cdots - a_n = 0$$

The scalar recurrence therefore shares the stability (or instability) of the matrix equation.

## Higher-order systems via block stacking

Any higher-order matrix difference equation can be reduced to first-order form by stacking current and lagged variables. A block matrix (a matrix whose entries are themselves matrices) handles the larger state. For $\mathbf{x}_t = \mathbf{A}\mathbf{x}_{t-1} + \mathbf{B}\mathbf{x}_{t-2}$:

$$\begin{bmatrix} \mathbf{x}_t \\ \mathbf{x}_{t-1} \end{bmatrix} = \begin{bmatrix} \mathbf{A} & \mathbf{B} \\ \mathbf{I} & \mathbf{0} \end{bmatrix} \begin{bmatrix} \mathbf{x}_{t-1} \\ \mathbf{x}_{t-2} \end{bmatrix}$$

Denoting the $2n \times 1$ stacked vector as $\mathbf{z}_t$ and the $2n \times 2n$ block matrix as $\mathbf{L}$, the solution is $\mathbf{z}_t = \mathbf{L}^t \mathbf{z}_0$. The original higher-order system is stable if and only if every eigenvalue of $\mathbf{L}$ has absolute value below 1.

## Nonlinear case: discrete Riccati equations

In linear-quadratic-Gaussian control, a nonlinear discrete dynamic Riccati equation governs the reverse evolution of the cost matrix $\mathbf{H}$:

$$\mathbf{H}_{t-1} = \mathbf{K} + \mathbf{A}'\mathbf{H}_t\mathbf{A} - \mathbf{A}'\mathbf{H}_t\mathbf{C}[\mathbf{C}'\mathbf{H}_t\mathbf{C} + \mathbf{R}]^{-1}\mathbf{C}'\mathbf{H}_t\mathbf{A}$$

with $\mathbf{H}$, $\mathbf{K}$, $\mathbf{A}$ $n \times n$, $\mathbf{C}$ $n \times k$, and $\mathbf{R}$ $k \times k$. No general closed form exists; the sequence is produced by iteration. In the usual backward-evolution setting the sequence is stable and converges to a fixed matrix $\mathbf{H}^*$ that may be irrational even when every other matrix is rational. Two closed-form cases are known: when $\mathbf{R} = \mathbf{0}$ and $n = k+1$ the equation reduces to a scalar rational difference equation, and when the transition matrix $\mathbf{A}$ is nonsingular the solution can be written in terms of eigenvalues of an auxiliary matrix (found numerically in general).

A related Riccati equation, $\mathbf{X}_{t+1} = -[\mathbf{E} + \mathbf{B}\mathbf{X}_t][\mathbf{C} + \mathbf{A}\mathbf{X}_t]^{-1}$ with all matrices $n \times n$, admits an explicit solution. The substitution $\mathbf{X}_t = \mathbf{N}_t\mathbf{D}_t^{-1}$ (valid at $t=0$ with $\mathbf{N}_0 = \mathbf{X}_0$, $\mathbf{D}_0 = \mathbf{I}$) converts the nonlinear recurrence into a linear one for the stacked pair $(\mathbf{N}_t, \mathbf{D}_t)$ driven by a constant $2n \times 2n$ matrix $\mathbf{J}$, giving $[\mathbf{N}_t, \mathbf{D}_t]^T = \mathbf{J}^t [\mathbf{N}_0, \mathbf{D}_0]^T$ by induction.

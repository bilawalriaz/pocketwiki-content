# Vector-valued function

A vector-valued function is a mathematical function whose range consists of vectors rather than single numbers. The input can be a scalar (a real or complex number), a vector, or several variables. The dimension of the domain has no connection to the dimension of the range: a scalar input can produce a 3D output, and a vector input can produce a scalar.

The most common case is a function of one real parameter, often representing time. In Cartesian 3-space the result is written either as a sum of scalar components times unit vectors $\mathbf{i}, \mathbf{j}, \mathbf{k}$ or as an ordered tuple:

$$\mathbf{r}(t) = f(t)\mathbf{i} + g(t)\mathbf{j} + h(t)\mathbf{k} = \langle f(t),\, g(t),\, h(t) \rangle$$

The component functions $f$, $g$, $h$ are ordinary scalar functions of the parameter $t$, and the domain of $\mathbf{r}$ is the intersection of their individual domains. Geometrically, each output $\mathbf{r}(t)$ is a position vector with its tail at the origin and its head at the point $(f(t), g(t), h(t))$. As $t$ varies, the head traces a curve. The helix $\langle 2\cos t,\, 4\sin t,\, t\rangle$ is the standard example: the first two components trace an ellipse while the third climbs linearly, producing a corkscrew path.

In2D the same pattern gives $\mathbf{r}(t) = \langle f(t), g(t) \rangle$.

## Linear and parametric forms

Linear and affine vector-valued functions are written compactly with matrices. If $A$ is an $n \times k$ matrix of parameters, $x$ is a $k \times 1$ input vector, and $b$ is an $n \times 1$ vector, then

$$\mathbf{y} = A\mathbf{x} + \mathbf{b}$$

covers both cases ($b = 0$ is linear; nonzero $b$ adds a translation). Multiple regression uses this form: predicted values are $\hat{\mathbf{y}} = X\hat{\boldsymbol{\beta}}$, where $X$ plays the role of $A$.

A surface in 3-space can be represented parametrically using two parameters $s$ and $t$:

$$(x, y, z) = \mathbf{F}(s, t) = (f(s,t),\, g(s,t),\, h(s,t))$$

This generalises to a surface embedded in $\mathbb{R}^n$ with $n$ scalar components of $\mathbf{F}$.

## Differentiation

Differentiation works componentwise. For a vector-valued function $\mathbf{r}(t) = \langle f(t),\, g(t),\, h(t)\rangle$, the derivative is

$$\frac{d\mathbf{r}}{dt} = \langle f'(t),\, g'(t),\, h'(t)\rangle$$

If $\mathbf{r}(t)$ represents a particle's position, the derivative is its velocity, and the second derivative is its acceleration.

The same rule extends to higher dimensions. A function $\mathbf{f}: \mathbb{R}^m \to \mathbb{R}^n$ has partial derivatives whose components form an $n \times m$ matrix called the Jacobian of $\mathbf{f}$. For a function $\mathbf{f}: \mathbb{R} \to X$ into a Hilbert space $X$ with orthonormal basis $\{e_i\}$, the componentwise formula still holds, but componentwise convergence does not guarantee convergence in the space's topology, so a componentwise derivative may fail to be the true derivative.

Product rules mirror the scalar rules. For a scalar $p$ and vector $\mathbf{a}$ both depending on a variable $q$:

$$\frac{\partial}{\partial q}(p\mathbf{a}) = \frac{\partial p}{\partial q}\mathbf{a} + p\frac{\partial \mathbf{a}}{\partial q}$$

The dot product rule is $\frac{\partial}{\partial q}(\mathbf{a}\cdot\mathbf{b}) = \frac{\partial \mathbf{a}}{\partial q}\cdot\mathbf{b} + \mathbf{a}\cdot\frac{\partial \mathbf{b}}{\partial q}$ and the cross product rule is $\frac{\partial}{\partial q}(\mathbf{a}\times\mathbf{b}) = \frac{\partial \mathbf{a}}{\partial q}\times\mathbf{b} + \mathbf{a}\times\frac{\partial \mathbf{b}}{\partial q}$.

If the vector depends on several scalar variables $q_r$, each itself a function of time, the total derivative adds the chain-rule contributions:

$$\frac{d\mathbf{a}}{dt} = \sum_{r=1}^n \frac{\partial \mathbf{a}}{\partial q_r}\frac{dq_r}{dt} + \frac{\partial \mathbf{a}}{\partial t}$$

## Reference frames

Differentiating a vector-valued function requires a choice of reference frame, because the result depends on the basis. The componentwise formula assumes the basis vectors $\mathbf{e}_1, \mathbf{e}_2, \mathbf{e}_3$ are constant in the frame of differentiation, which holds for fixed Cartesian systems but fails in rotating or moving frames.

If the basis $\{\mathbf{e}_i\}$ is constant in frame $E$ but not in frame $N$, the time derivative in $N$ gains an extra term from the changing basis:

$$\frac{{}^N d\mathbf{a}}{dt} = \sum_i \frac{da_i}{dt}\mathbf{e}_i + \sum_i a_i \frac{{}^N d\mathbf{e}_i}{dt}$$

The first sum is the derivative in frame $E$. The second sum equals the angular velocity of frame $E$ relative to frame $N$ cross-multiplied with $\mathbf{a}$, giving the transport theorem

$$\frac{{}^N d\mathbf{a}}{dt} = \frac{{}^E d\mathbf{a}}{dt} + {}^N\boldsymbol{\omega}^E \times \mathbf{a}$$

A practical use is finding the inertial velocity ${}^N\mathbf{v}^R$ of a rocket $R$ from its ground-measured velocity ${}^E\mathbf{v}^R$:

$${}^N\mathbf{v}^R = {}^E\mathbf{v}^R + {}^N\boldsymbol{\omega}^E \times \mathbf{r}^R$$

where ${}^N\boldsymbol{\omega}^E$ is Earth's angular velocity relative to the inertial frame.

## Vector fields

A vector field is a vector-valued function whose domain is a region of space rather than a single parameter. On $\mathbb{R}^n$ it assigns an $n$-tuple of real numbers to each point, so it carries a magnitude and direction at every location. Vector fields visualise as arrows attached to points and model wind velocity, magnetic force, and gravitational force. A space curve's position vector is defined only on a subset of the ambient space, while a vector field fills an open region. The calculus of vector fields, including line integrals, divergence, and curl, extends the ordinary calculus of scalar fields to the vector setting.

Source: adapted from "Vector-valued function" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Vector-valued_function

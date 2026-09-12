# Cauchy–Schwarz inequality

The Cauchy–Schwarz inequality bounds the inner product of two vectors by the product of their lengths. For vectors **u** and **v** in any inner product space,

$$|\langle \mathbf{u}, \mathbf{v} \rangle| \leq \|\mathbf{u}\| \, \|\mathbf{v}\|,$$

with equality if and only if **u** and **v** are linearly dependent (one is a scalar multiple of the other, or one is the zero vector). An inner product is a generalisation of the dot product: a way to pair two vectors that yields a number and behaves linearly. The induced norm is $\|\mathbf{u}\| = \sqrt{\langle \mathbf{u}, \mathbf{u} \rangle}$, which measures length. The inequality was first stated for finite sums by Cauchy in 1821, then extended to integrals by Bunyakovsky in 1859 and Schwarz in 1888, and is now used across analysis, geometry, probability, and combinatorics.

## The same inequality in different settings

In the Euclidean plane, where the inner product is the dot product, the inequality becomes

$$(u_1 v_1 + u_2 v_2)^2 \leq (u_1^2 + u_2^2)(v_1^2 + v_2^2),$$

which is the statement that $|\cos\theta| \leq 1$ for the angle $\theta$ between the two vectors. The form extends to $\mathbb{R}^n$ and to $\mathbb{C}^n$ using the canonical complex inner product $\langle \mathbf{u}, \mathbf{v} \rangle = \sum u_k \overline{v_k}$. For square-integrable functions, the sum becomes an integral:

$$\left|\int f(x)\,\overline{g(x)}\,dx\right|^2 \leq \int |f(x)|^2\,dx \int |g(x)|^2\,dx.$$

The inequality is therefore the same object in finite-dimensional, sequence, and function settings, with "sum" replaced by "integral" when the vectors are functions.

## Why it is true

A short proof for real vectors uses the quadratic polynomial

$$p(x) = \sum_{i=1}^{n} (u_i x + v_i)^2 = \Big(\sum u_i^2\Big) x^2 + 2\Big(\sum u_i v_i\Big) x + \sum v_i^2.$$

Because $p(x) \geq 0$ for all real $x$, the discriminant is non-positive:

$$\Big(\sum u_i v_i\Big)^2 - \Big(\sum u_i^2\Big)\Big(\sum v_i^2\Big) \leq 0,$$

which rearranges into the inequality. A geometric proof notes that the squared length of the component of **u** perpendicular to **v** is $\|\mathbf{u}\|^2 - |\langle \mathbf{u},\mathbf{v}\rangle|^2/\|\mathbf{v}\|^2 \geq 0$, since lengths are non-negative.

## Consequences

The triangle inequality follows directly. Expanding $\|\mathbf{u} + \mathbf{v}\|^2$ and applying Cauchy–Schwarz to bound $2|\langle \mathbf{u},\mathbf{v}\rangle|$ by $2\|\mathbf{u}\|\|\mathbf{v}\|$ yields $\|\mathbf{u} + \mathbf{v}\| \leq \|\mathbf{u}\| + \|\mathbf{v}\|$.

Because the ratio $\langle \mathbf{u},\mathbf{v}\rangle / (\|\mathbf{u}\|\|\mathbf{v}\|)$ always lies in $[-1, 1]$, the formula $\cos\theta = \langle \mathbf{u},\mathbf{v}\rangle / (\|\mathbf{u}\|\|\mathbf{v}\|)$ defines an angle in any real inner product space, giving Hilbert spaces a Euclidean geometry.

In probability, treating random variables as vectors with inner product $\langle X, Y \rangle = \mathbb{E}(XY)$ produces the covariance inequality $|\operatorname{Cov}(X,Y)|^2 \leq \operatorname{Var}(X)\operatorname{Var}(Y)$. In graph theory, the bound on sums of squares proves Mantel's theorem: a triangle-free graph on $n$ vertices has at most $\lfloor n^2/4 \rfloor$ edges. In linear algebra, Cauchy–Schwarz is used in the proof of the spectral theorem for self-adjoint operators, which says such operators can be diagonalised by an orthonormal basis.

A useful finite-sum consequence is Sedrakyan's inequality (also called Titu's or Engel's form): for positive reals $v_i$,

$$\frac{\left(\sum u_i\right)^2}{\sum v_i} \leq \sum \frac{u_i^2}{v_i},$$

obtained by substituting $u_i' = u_i/\sqrt{v_i}$ and $v_i' = \sqrt{v_i}$ into the dot-product version. Hölder's inequality generalises Cauchy–Schwarz to $L^p$ norms, with Cauchy–Schwarz as the special case $p = q = 2$.

Source: adapted from "Cauchy–Schwarz inequality" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Cauchy%E2%80%93Schwarz_inequality

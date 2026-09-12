# Fundamental theorem of calculus

The fundamental theorem of calculus ties together the two central operations of calculus: differentiation (computing slopes or rates of change) and integration (computing areas or accumulated quantities). The two operations look unrelated, but the theorem shows they are inverses, undoing each other the way addition undoes subtraction.

## The core idea

If you know a quantity's rate of change, adding up all those small rates over an interval recovers the total change in the quantity. Conversely, if you accumulate a rate from a fixed starting point up to a variable endpoint, the rate at which that accumulated amount grows is the original rate itself.

Picture driving while watching only the speedometer. Each second, distance traveled is roughly speed × time. Summing those pieces gives total distance. That sum, in the limit of infinitesimally small time slices, is the integral of velocity. Velocity is the derivative of position, so the integral of the derivative recovers net change, and the derivative of the integral recovers the original function. This is the everyday intuition behind the theorem.

## Formal statement

**First part.** If $f$ is continuous on $[a,b]$, define
$$F(x) = \int_a^x f(t)\,dt.$$
Then $F$ is differentiable on $(a,b)$ and $F'(x) = f(x)$. The integral of a continuous function from a fixed start is an antiderivative, a function whose derivative recovers $f$.

**Second part (the Newton–Leibniz formula).** If $F$ is any antiderivative of $f$ on $[a,b]$, so $F'(x) = f(x)$, and $f$ is integrable, then
$$\int_a^b f(x)\,dx = F(b) - F(a).$$
The definite integral equals the change in any antiderivative across the interval. Adding a constant to $F$ leaves both sides unchanged, so the choice of antiderivative does not matter.

## Why it matters

Before the theorem, areas and slopes were treated as separate problems. Calculus became a unified subject once mathematicians realized these two operations are two sides of the same coin.

The practical payoff is large. Definite integrals that would otherwise require numerical approximation can often be evaluated exactly by finding any antiderivative and subtracting its endpoint values. For instance,
$$\int_2^5 x^2\,dx = \left[\tfrac{x^3}{3}\right]_2^5 = \tfrac{125}{3} - \tfrac{8}{3} = 39.$$

## Sketch of the geometric idea

For the first part, let $A(x)$ be the area under a continuous curve $y = f(x)$ between $0$ and $x$. The thin strip between $x$ and $x+h$ has area $A(x+h) - A(x)$ and is approximately $f(x)\cdot h$. Dividing by $h$ and letting $h \to 0$ gives
$$\lim_{h \to 0}\frac{A(x+h)-A(x)}{h} = f(x),$$
which is exactly $A'(x)$. Differentiating the area function recovers the original height function.

For the second part, split $[a,b]$ into small subintervals. On each $[x_{i-1}, x_i]$, the mean value theorem gives a point $c_i$ with
$$F(x_i)-F(x_{i-1}) = F'(c_i)(x_i - x_{i-1}) = f(c_i)\,\Delta x_i.$$
Telescoping the left side yields $F(b) - F(a)$, while the right side becomes a Riemann sum. As the partition refines, the sum converges to $\int_a^b f(x)\,dx$.

## Relationship between the parts

The second part follows from the first together with the mean value theorem. The first part does not follow from the second: knowing that antiderivatives yield definite integrals does not prove every continuous function has an antiderivative. That guarantee comes only from the first part.

This distinction matters at the edges. Some integrable functions have no antiderivative at all, including discontinuous ones, and some continuous functions have antiderivatives with no elementary closed form, such as $e^{-x^2}$. Other functions have antiderivatives yet fail to be Riemann integrable; Volterra's function is the standard example. The theorem is precise about which guarantees it provides and under which conditions.

## Generalizations

If $f$ is merely Lebesgue integrable and continuous at a point $x_0$, then $F(x) = \int_a^x f$ is differentiable at $x_0$ with $F'(x_0) = f(x_0)$. Relaxing further, $F' = f$ holds almost everywhere, which is Lebesgue's differentiation theorem. The Newton–Leibniz formula remains valid for the Henstock–Kurzweil integral, which integrates more functions than Lebesgue's version. In higher dimensions the fundamental idea becomes the generalized Stokes theorem: for a smooth $(n-1)$-form $\omega$ on an oriented $n$-dimensional manifold $M$ with boundary $\partial M$,
$$\int_M d\omega = \int_{\partial M} \omega,$$
which recovers the divergence theorem, gradient theorem, and classical Stokes theorem as special cases.

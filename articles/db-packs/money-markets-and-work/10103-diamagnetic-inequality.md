# Diamagnetic inequality

The diamagnetic inequality bounds the gradient of the modulus of a complex function by its covariant derivative (a derivative modified by a connection so it transforms correctly under a local phase change). For almost every $x \in \mathbb{R}^n$,

$$|\nabla |f|(x)| \le |(\nabla + iA)f(x)|,$$

so the Sobolev norm (the $L^2$ norm of a function together with its derivatives) of $|f|$ is bounded by the same norm of the covariant derivative of $f$. Physically, a charged particle in a magnetic field has more ground state energy than the same particle in a vacuum, because the magnetic potential contributes a non-negative amount to the kinetic term.

## Setup

Work in $\mathbb{R}^n$ with the Lebesgue space $L^2(\mathbb{R}^n)$ of square-integrable functions and the Sobolev space $H^1(\mathbb{R}^n)$ of functions in $L^2$ whose derivatives are also in $L^2$. Let $A_1, \dots, A_n$ be real-valued measurable functions with $A_j \in L^2_{\text{loc}}(\mathbb{R}^n)$ (square-integrable on every bounded region), and let $f$ be complex-valued with $f, (\partial_1 + iA_1)f, \dots, (\partial_n + iA_n)f \in L^2(\mathbb{R}^n)$. Then the inequality above holds for almost every $x$, and $|f| \in H^1(\mathbb{R}^n)$.

## Why the inequality holds

Following Lieb and Loss, the assumptions force $\partial_j |f| \in L^1_{\text{loc}}(\mathbb{R}^n)$ in the sense of distributions. For almost every $x$ with $f(x) \ne 0$,

$$\partial_j |f|(x) = \operatorname{Re}\!\left(\frac{\overline{f}(x)}{|f(x)|}\,\partial_j f(x)\right),$$

and $\partial_j |f|(x) = 0$ where $f(x) = 0$.

The magnetic term drops out of the comparison because

$$\operatorname{Re}\!\left(\frac{\overline{f}(x)}{|f(x)|}\, iA_j f(x)\right) = \operatorname{Re}(iA_j) = 0,$$

since each $A_j$ is real. Writing $\mathbf{D} = \nabla + iA$ and using $\operatorname{Re}(z) \le |z|$ gives

$$\nabla |f|(x) = \operatorname{Re}\!\left(\frac{\overline{f}(x)}{|f(x)|}\,\mathbf{D} f(x)\right) \le \left|\frac{\overline{f}(x)}{|f(x)|}\,\mathbf{D} f(x)\right| = |\mathbf{D} f(x)|$$

for almost every $x$ with $f(x) \ne 0$, and the bound extends to the vanishing case.

## Application to line bundles

Let $p: L \to \mathbb{R}^n$ be a $U(1)$ line bundle (a complex one-dimensional vector bundle acted on by local phase rotations) with real-valued connection 1-form $A$. The covariant derivative acts on a section $f$ by $\mathbf{D} f_j = (\partial_j + iA_j) f$, so the inequality becomes $|\nabla |f|(x)| \le |\mathbf{D} f(x)|$.

The case of physical interest takes $\mathbb{R}^n$ as Minkowski spacetime. Since the gauge group of electromagnetism is $U(1)$, connection 1-forms for $L$ are exactly the electromagnetic four-potentials on $\mathbb{R}^n$. With $F = dA$ the electromagnetic field tensor and $\phi$ a section of $L$, the massless Maxwell–Klein–Gordon system is

$$\begin{cases} \partial^\mu F_{\mu\nu} = \operatorname{Im}(\phi\, \mathbf{D}_\nu \phi) \\ \mathbf{D}^\mu \mathbf{D}_\mu \phi = 0, \end{cases}$$

with conserved energy

$$\frac{\|F(t)\|_{L^2_x}^2}{2} + \frac{\|\mathbf{D}\phi(t)\|_{L^2_x}^2}{2}.$$

The kinetic term $\|\mathbf{D}\phi\|_{L^2}^2$ depends on $A$, and turning off electromagnetism (taking $A = 0$) minimises this energy because $|\nabla |\phi|| \le |\mathbf{D}\phi|$.

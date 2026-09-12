# Complex number

## Overview
A complex number is an element of a number system extending the real numbers by an imaginary unit $i$ satisfying $i^2 = -1$. Every complex number is uniquely expressed as $a + bi$ with real $a$ (real part) and $b$ (imaginary part). The set $\mathbb{C}$ forms an algebraically closed field: every non-constant polynomial with complex coefficients has a root in $\mathbb{C}$ (Fundamental Theorem of Algebra). Complex numbers simultaneously constitute a commutative algebra over $\mathbb{R}$, a Euclidean vector space of dimension two (the complex plane), and a complete metric space. This structure allows geometric interpretation of arithmetic (addition as translation, multiplication as rotation and dilation) and underpins complex analysis, which provides powerful tools for physics, engineering, and number theory.

## Timeline
- **1st century AD** — Hero of Alexandria encounters $\sqrt{81-144}$ in *Stereometrica* but replaces it with $\sqrt{144-81}$.
- **1500s** — Scipione del Ferro and Gerolamo Cardano create an algorithm for solving cubic equations yielding one real and two imaginary solutions; imaginary solutions are ignored.
- **1545** — Gerolamo Cardano publishes *Ars Magna*, conceiving complex numbers while solving cubic equations (casus irreducibilis), calling them "subtle as they are useless."
- **1572** — Rafael Bombelli develops systematic rules for complex arithmetic in his *Algebra*.
- **1637** — René Descartes coins the term "imaginary" for $\sqrt{-1}$, stressing their "unreal nature."
- **1730** — Abraham de Moivre states de Moivre's formula $(\cos \theta + i\sin \theta)^n = \cos n\theta + i\sin n\theta$.
- **1748** — Leonhard Euler publishes Euler's formula $e^{i\theta} = \cos \theta + i\sin \theta$ in *Introductio in analysin infinitorum*.
- **1797** — Carl Friedrich Gauss publishes an essentially topological proof of the Fundamental Theorem of Algebra, but expresses doubts about "the true metaphysics of the square root of −1".
- **1799** — Caspar Wessel presents the geometric interpretation of complex numbers as points in a plane.
- **1806** — Jean-Robert Argand independently publishes the complex plane (Argand diagram) and a rigorous proof of the Fundamental Theorem of Algebra.
- **1831** — Gauss publishes his major treatise on complex numbers, establishing modern notation ($i$, "complex number," "norm") and confident usage.
- **1830s onward** — William Rowan Hamilton develops a more abstract formalism for complex numbers and extends it to the theory of quaternions.
- **1825 onward** — Augustin-Louis Cauchy commences development of complex analysis; Bernhard Riemann later brings it to a high state of completion (1850s).
- **1927** — Wilhelm Wirtinger achieves important results in complex multivariate calculus, systematizing work begun early in the 20th century.

## Body

### Definition and Algebraic Structure
A complex number is an expression $z = a + bi$ where $a,b \in \mathbb{R}$ and $i$ is a symbol with $i^2 = -1$. The real part is $\operatorname{Re}(z)=a$; the imaginary part is $\operatorname{Im}(z)=b$ (a real number). The set $\mathbb{C}$ is a field containing $\mathbb{R}$ as a subfield ($a \mapsto a+0i$). Addition and multiplication follow from $i^2=-1$ and the distributive, commutative, and associative laws:
$$(a+bi)+(c+di) = (a+c)+(b+d)i$$
$$(a+bi)(c+di) = (ac-bd)+(ad+bc)i$$
Every non-zero $z$ has a multiplicative inverse, making $\mathbb{C}$ a field. $\mathbb{C}$ is also a real vector space of dimension two with basis $\{1, i\}$, identifying $z$ with the ordered pair $(a,b)$ in the **complex plane** (Argand diagram), where the real axis is horizontal and the imaginary axis vertical.

### Conjugation, Absolute Value, and Polar Form
The **complex conjugate** of $z=x+yi$ is $\overline{z}=x-yi$ (reflection across the real axis). The product $z\overline{z}=x^2+y^2$ is a non-negative real, defining the **absolute value** (modulus) $|z| = \sqrt{x^2+y^2}$, the Euclidean distance from the origin. The **argument** $\arg z = \varphi$ is the angle from the positive real axis, defined up to multiples of $2\pi$; the principal value lies in $(-\pi, \pi]$.

These yield the **polar form**: $z = r(\cos\varphi + i\sin\varphi)$ with $r=|z|$, often abbreviated $r\operatorname{cis}\varphi$ or $r\angle\varphi$ (electronics). In polar form, multiplication and division become geometric: moduli multiply/divide and arguments add/subtract.
$$z_1 z_2 = r_1 r_2 (\cos(\varphi_1+\varphi_2) + i\sin(\varphi_1+\varphi_2))$$
$$\frac{z_1}{z_2} = \frac{r_1}{r_2} (\cos(\varphi_1-\varphi_2) + i\sin(\varphi_1-\varphi_2))$$

**De Moivre's formula** gives powers: $z^n = r^n(\cos n\varphi + i\sin n\varphi)$. The $n$ distinct $n$-th roots of $z\neq 0$ are $\sqrt[n]{r}(\cos\frac{\varphi+2k\pi}{n} + i\sin\frac{\varphi+2k\pi}{n})$ for $k=0,\dots,n-1$. The $n$-th root is thus an $n$-valued function.

### Fundamental Theorem of Algebra
Proved by Gauss (1797) and Argand (1806), the theorem states: every non-constant polynomial $a_n z^n + \dots + a_1 z + a_0 = 0$ with complex coefficients has at least one complex root. Consequently, $\mathbb{C}$ is **algebraically closed** (and is the algebraic closure of $\mathbb{R}$). This fails for $\mathbb{Q}$ (e.g., $x^2-2$) and $\mathbb{R}$ (e.g., $x^2+4$).

### Abstract Algebraic Definitions
$\mathbb{C}$ can be defined abstractly as the unique (up to isomorphism) algebraic extension field of $\mathbb{R}$ generated by an element $i$ with $i^2=-1$. Equivalently, it is the splitting field of $x^2+1$ over $\mathbb{R}$.

**Construction as quotient ring:** $\mathbb{C} \cong \mathbb{R}[X]/(X^2+1)$. Polynomials in $\mathbb{R}[X]$ are evaluated at $X=i$; the kernel is the ideal generated by the irreducible $X^2+1$, and the quotient is a field isomorphic to $\mathbb{C}$.

**Matrix representation:** $a+bi \mapsto \begin{pmatrix} a & -b \\ b & a \end{pmatrix}$. This is a ring isomorphism onto a subring of $2\times 2$ real matrices. The determinant equals $|z|^2$; the transpose corresponds to conjugation. Polar form $r(\cos\theta+i\sin\theta)$ maps to scaled rotation matrices.

### Complex Analysis
Complex analysis studies functions $f: \mathbb{C} \to \mathbb{C}$. Convergence is defined via the metric $d(z_1,z_2)=|z_1-z_2|$, making $\mathbb{C}$ a complete metric space.

**Elementary functions** are defined by power series convergent everywhere:
- Exponential: $\exp z = \sum_{n=0}^\infty z^n/n!$. Euler's formula: $\exp(i\varphi)=\cos\varphi+i\sin\varphi$; Euler's identity: $e^{i\pi}=-1$.
- Logarithm: $\log w = \ln|w| + i\arg w$. Because $\arg$ is multi-valued (period $2\pi$), $\log$ is multi-valued. The principal value restricts $\arg$ to $(-\pi,\pi]$, yielding a branch cut on the negative real axis.
- Trigonometric/hyperbolic functions: Defined by their series or via $\sin z = (\exp(iz)-\exp(-iz))/(2i)$, etc. For $z=x+iy$, e.g., $\sin z = \sin x\cosh y + i\cos x\sinh y$.

**Holomorphic functions:** $f$ is holomorphic at $z_0$ if $\lim_{z\to z_0} (f(z)-f(z_0))/(z-z_0)$ exists. This is strictly stronger than real differentiability; e.g., $f(z)=\overline{z}$ is real-differentiable but not complex-differentiable. A real-differentiable function is holomorphic iff it satisfies the Cauchy–Riemann equations $\partial f/\partial\overline{z}=0$. Holomorphic functions are rigid: the identity theorem states that two such functions agreeing on an arbitrarily small open set are identical everywhere.

### Applications
**Geometry:** Triangle shape $S(u,v,w) = (u-w)/(u-v)$ is invariant under translation/dilation (similarity). **Fractals:** Mandelbrot set ($z_{n+1}=z_n^2+c$ bounded) and Julia sets. **Marden's theorem:** Foci of a triangle's Steiner inellipse are roots of the derivative of $(x-a)(x-b)(x-c)=0$.

**Algebraic/Analytic Number Theory:** $\mathbb{C}$ contains all algebraic numbers (roots of rational polynomials). Geometric intuition in $\mathbb{C}$ aids algebraic problems (e.g., impossibility of constructing a regular nonagon with compass/straightedge). The Riemann zeta function $\zeta(s)$ encodes prime distribution.

**Applied Mathematics:**
- **Improper integrals:** Computed via contour integration in the complex plane.
- **Differential/difference equations:** Solutions built from $e^{rt}$ or $r^t$ where $r$ are complex roots of the characteristic equation.
- **Linear algebra:** $\mathbb{C}$ algebraically closed $\Rightarrow$ every complex square matrix has eigenvalues, enabling eigendecomposition, matrix powers, and exponentials. Hermitian/unitary matrices generalize symmetric/orthogonal ones.

**Control Theory:** Laplace transform maps time domain to complex frequency domain. Stability determined by pole locations: right half-plane $\Rightarrow$ unstable; left half-plane $\Rightarrow$ stable; imaginary axis $\Rightarrow$ marginal. Root locus, Nyquist, and Nichols plots use the complex plane.

**Signal Analysis:** Periodic signals represented as $X(t)=Ae^{i\omega t}=ae^{i(\omega t+\phi)}$; physical signal is $\operatorname{Re}(X(t))$. Amplitude $=|A|$, phase $=\arg A$. Fourier/wavelet analysis uses this for digital signal/image processing (compression, restoration). AM radio sidebands derived via $\cos((\omega+\alpha)t)+\cos((\omega-\alpha)t) = 2\cos(\alpha t)\cos(\omega t)$ using complex exponentials.

**Physics:**
- **Electromagnetism/EE:** Phasor calculus uses impedance $Z$ (complex resistance). $j$ replaces $i$ to avoid confusion with current. AC voltage $V(t)=V_0 e^{j\omega t}$; measurable $v(t)=\operatorname{Re}(V(t))$.
- **Fluid dynamics:** Complex functions describe 2D potential flow.
- **Quantum mechanics:** Intrinsic; state space is a complex Hilbert space. Schrödinger equation and Heisenberg matrix mechanics use complex numbers.
- **Relativity:** Imaginary time component simplifies some spacetime metrics (standard in quantum field theory). Spinors generalize tensors using complex numbers.

### Characterizations and Generalizations
**Algebraic characterization:** $\mathbb{C}$ is the unique (up to isomorphism) field of characteristic 0, transcendence degree continuum over $\mathbb{Q}$, and algebraically closed. The algebraic closure of $\mathbb{Q}_p$ (p-adics) shares these properties, so $\overline{\mathbb{Q}_p} \cong \mathbb{C}$ as fields (not topological fields).

**Topological field characterization:** $\mathbb{C}$ is characterized as a connected, locally compact topological field containing a subset $P$ (positive reals) closed under addition, multiplication, inversion, and satisfying an order-like condition, plus an involution $x\mapsto x^*$ (conjugation) with $xx^*\in P$. The only connected locally compact topological fields are $\mathbb{R}$ and $\mathbb{C}$; $\mathbb{C}^\times$ is connected, $\mathbb{R}^\times$ is not.

**Other number systems (Cayley–Dickson construction):** Iteratively extending $\mathbb{R}\to\mathbb{C}\to\mathbb{H}$ (quaternions)$\to\mathbb{O}$ (octonions)$\to\dots$ loses properties: $\mathbb{C}$ is not ordered ($i^2=-1$); $\mathbb{H}$ loses commutativity; $\mathbb{O}$ loses associativity. $\mathbb{R},\mathbb{C},\mathbb{H},\mathbb{O}$ are the only normed division algebras over $\mathbb{R}$ (Hurwitz). Split-complex numbers ($\mathbb{R}[x]/(x^2-1)$) have four solutions to $a^2=1$. p-adic complex numbers $\mathbb{C}_p$ are the completion of $\overline{\mathbb{Q}_p}$, algebraically closed but not locally compact. $\mathbb{R}, \mathbb{Q}_p$, and their finite extensions (including $\mathbb{C}$) are **local fields**.

## Terms
- ****Imaginary unit $i$**** — Symbol satisfying $i^2 = -1$; extends $\mathbb{R}$ to $\mathbb{C}$.
- ****Complex conjugate $\overline{z}$**** — For $z=x+yi$, $\overline{z}=x-yi$; reflection across the real axis in the complex plane.
- ****Absolute value (modulus) $|z|$**** — $\sqrt{x^2+y^2}$; Euclidean distance from origin to $z$ in the complex plane.
- ****Argument $\arg z$**** — Angle $\varphi$ from positive real axis to radius vector of $z$; defined modulo $2\pi$.
- ****Polar form**** — Representation $z = r(\cos\varphi + i\sin\varphi)$ with $r=|z|$, $\varphi=\arg z$.
- ****Algebraically closed field**** — A field in which every non-constant polynomial has a root; $\mathbb{C}$ is the algebraic closure of $\mathbb{R}$.
- ****Holomorphic function**** — Complex-differentiable at a point (limit of difference quotient exists); equivalent to satisfying Cauchy–Riemann equations.
- ****Branch cut**** — A curve (e.g., negative real axis) removed from the domain to make a multi-valued function (like $\log z$) single-valued and continuous.
- ****Impedance**** — Complex generalization of resistance in AC circuits, unifying resistors, capacitors, and inductors via phasor calculus.
- ****Cayley–Dickson construction**** — Iterative doubling process generating $\mathbb{C}$, quaternions $\mathbb{H}$, octonions $\mathbb{O}$, etc., each step losing algebraic properties (order, commutativity, associativity).

## Debates and open questions
- **Ontological status of $i$:** Historically debated (Descartes' "imaginary," Gauss's "lateral units"). The source notes Gauss (1831) argued better terminology ("direct, inverse, lateral") would have avoided "mysterious darkness."
- **Consistency of algebraic identities:** The identity $\sqrt{a}\sqrt{b}=\sqrt{ab}$ holds for non-negative reals but fails for negative $a,b$ (e.g., $\sqrt{-1}\sqrt{-1} \neq \sqrt{1}$). This "bedeviled Leonhard Euler" and motivated the dedicated symbol $i$.
- **Uniqueness of roots:** Unlike positive reals (unique positive $n$-th root), complex $n$-th roots are $n$-valued with no canonical choice; the $n$-th root is an $n$-valued function.
- **Power/logarithm identities:** Complex numbers do not generally satisfy unmodified identities like $a^{bc}=(a^b)^c$ when treated as single-valued; both sides are multi-valued sets with the left a subset of the right.
- **Topological vs. algebraic isomorphism:** The algebraic closure of $\mathbb{Q}_p$ is isomorphic to $\mathbb{C}$ as a field (requiring Axiom of Choice) but *not* as a topological field; $\mathbb{C}_p$ (its completion) is not locally compact.
- **Physical interpretation of imaginary time:** In relativity, taking the time component as imaginary simplifies metrics but is "no longer standard in classical relativity," though essential in quantum field theory and spinor formalism.

Source: adapted from "Complex number" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Complex_number

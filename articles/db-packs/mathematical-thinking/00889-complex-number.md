# Complex number

A complex number is a number of the form $a+bi$, where $a$ and $b$ are real numbers and $i$ is a symbol with the single defining property $i^2=-1$. The real numbers appear as the special case $b=0$. The set of all complex numbers is written $\mathbb{C}$.

## Arithmetic

Addition and multiplication follow the ordinary rules of algebra, with $i^2$ replaced by $-1$ wherever it appears:

$$(a+bi)+(c+di) = (a+c)+(b+d)i$$
$$(a+bi)(c+di) = (ac-bd)+(ad+bc)i$$

Every nonzero $z$ has a multiplicative inverse, so $\mathbb{C}$ is a *field*: addition, subtraction, multiplication, and division (by nonzero values) all behave as in $\mathbb{R}$.

## The complex plane

Identifying $z=a+bi$ with the point $(a,b)$ gives the *complex plane* (Argand diagram), with the real part on the horizontal axis and the imaginary part on the vertical axis. In this picture, addition is vector addition, and several standard constructions fall into place:

- The *conjugate* $\overline{z}=a-bi$ is the reflection of $z$ across the real axis.
- The *modulus* $|z|=\sqrt{a^2+b^2}$ is the Euclidean distance from the origin.
- The *argument* $\arg z=\varphi$ is the angle from the positive real axis to the radius vector, defined up to multiples of $2\pi$.

Multiplication becomes geometric. If $z_1$ has modulus $r_1$ and argument $\varphi_1$, and $z_2$ has $r_2$ and $\varphi_2$, then $z_1z_2$ has modulus $r_1r_2$ and argument $\varphi_1+\varphi_2$, while $z_1/z_2$ has modulus $r_1/r_2$ and argument $\varphi_1-\varphi_2$. Multiplying by a complex number scales by its modulus and rotates by its argument.

This description yields the *polar form* $z=r(\cos\varphi+i\sin\varphi)$, abbreviated $r\,\mathrm{cis}\,\varphi$ or $r\angle\varphi$, and two central identities:

- *De Moivre's formula:* $z^n=r^n(\cos n\varphi+i\sin n\varphi)$.
- *Euler's formula:* $e^{i\varphi}=\cos\varphi+i\sin\varphi$, with the special case $e^{i\pi}+1=0$.

Because the argument is only defined modulo $2\pi$, every nonzero $z$ has exactly $n$ distinct $n$-th roots, evenly spaced at angles $(\varphi+2k\pi)/n$ for $k=0,1,\dots,n-1$.

## Why $\mathbb{C}$ exists: the Fundamental Theorem of Algebra

The real numbers cannot solve $x^2+1=0$. In $\mathbb{C}$, every non-constant polynomial with complex coefficients has at least one complex root, so the polynomial splits completely into linear factors. A field with this property is *algebraically closed*, and $\mathbb{C}$ is the algebraic closure of $\mathbb{R}$. Adjoining a single root of $x^2+1$ to $\mathbb{R}$ already produces a field with this property.

## Other ways to build the same field

Three constructions give the same object up to isomorphism:

- *Algebraic extension:* $\mathbb{C}=\mathbb{R}(i)$ where $i^2=-1$.
- *Quotient ring:* $\mathbb{C}\cong\mathbb{R}[X]/(X^2+1)$, polynomials in one real variable modulo $X^2+1=0$.
- *Matrix form:* $a+bi\mapsto\begin{pmatrix}a&-b\\b&a\end{pmatrix}$ embeds $\mathbb{C}$ in the $2\times 2$ real matrices; the determinant equals $|z|^2$ and the transpose corresponds to conjugation.

## Complex analysis

The metric $d(z_1,z_2)=|z_1-z_2|$ makes $\mathbb{C}$ a complete metric space, so limits, continuity, and convergence of sequences and series work as in $\mathbb{R}^2$.

A function $f:\mathbb{C}\to\mathbb{C}$ is *holomorphic* at $z_0$ when the limit $\lim_{z\to z_0}(f(z)-f(z_0))/(z-z_0)$ exists. This is strictly stronger than real differentiability, because the limit must agree along every direction in the complex plane. For $f=u+iv$ with continuous partials, holomorphy is equivalent to the Cauchy–Riemann equations $\partial u/\partial x=\partial v/\partial y$ and $\partial u/\partial y=-\partial v/\partial x$. A consequence is the *identity theorem*: two holomorphic functions agreeing on any open set agree everywhere.

The elementary functions extend to $\mathbb{C}$ through their power series. The exponential $\exp z=\sum z^n/n!$ converges everywhere, and Euler's formula gives $\exp(i\varphi)=\cos\varphi+i\sin\varphi$. The logarithm $\log w=\ln|w|+i\arg w$ is multi-valued because $\arg$ is multi-valued; choosing $\arg$ in $(-\pi,\pi]$ selects the principal branch, with a *branch cut* along the negative real axis to keep the function continuous.

## Applications

- *Linear algebra.* Every complex square matrix has eigenvalues, since the characteristic polynomial splits over $\mathbb{C}$. This underlies eigendecomposition, matrix exponentials, and Hermitian/unitary matrices.
- *Differential and difference equations.* Solutions are built from terms $e^{rt}$ or $r^t$ where $r$ is a complex root of the characteristic equation, even when coefficients and initial data are real.
- *Improper integrals.* Many real integrals that resist elementary methods become tractable by contour integration in the complex plane.
- *Number theory.* The Riemann zeta function $\zeta(s)$, which encodes the distribution of primes, is a complex-analytic object.
- *Signal processing and control.* Fourier analysis writes signals as sums of complex exponentials $e^{i\omega t}$; the Laplace transform places control systems in the complex-frequency plane, where pole locations determine stability.
- *Electrical engineering.* Impedance $Z$ generalises resistance to AC circuits in a single phasor; engineers write the imaginary unit as $j$ to avoid confusion with current $i$.
- *Physics.* Quantum mechanics is built on complex Hilbert spaces; the Schrödinger equation and Heisenberg's matrix mechanics both require complex amplitudes. Complex functions also describe two-dimensional potential flow in fluid dynamics.

## Generalisations and cousins

The Cayley–Dickson construction produces larger number systems by repeated doubling: $\mathbb{R}\to\mathbb{C}\to\mathbb{H}$ (quaternions)$\to\mathbb{O}$ (octonions). Each step loses an algebraic property: $\mathbb{C}$ cannot be ordered (since $i^2=-1$ has no real square root), $\mathbb{H}$ loses commutativity of multiplication, $\mathbb{O}$ loses associativity. Hurwitz's theorem states that $\mathbb{R},\mathbb{C},\mathbb{H},\mathbb{O}$ are the only normed division algebras over the reals.

The *split-complex numbers* $\mathbb{R}[x]/(x^2-1)$ have four square roots of $1$. The *$p$-adic complex numbers* $\mathbb{C}_p$ are algebraically closed but not locally compact; as bare fields, $\mathbb{C}_p$ and $\mathbb{C}$ are isomorphic, though not as topological fields.

Source: adapted from "Complex number" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Complex_number

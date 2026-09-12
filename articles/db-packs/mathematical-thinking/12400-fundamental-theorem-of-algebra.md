# Fundamental theorem of algebra

Every non-constant polynomial in one variable, with complex coefficients, has at least one complex root. Equivalently, the field of complex numbers is algebraically closed: every such polynomial factors completely as a constant times linear factors, so a degree-$n$ polynomial has exactly $n$ complex roots counted with multiplicity. Polynomials with real coefficients are included, because every real number is a complex number with imaginary part zero.

A root is a number $r$ with $p(r) = 0$, and multiplicity lets a root repeat: if $p(z) = (z-2)^2(z+1)$, then 2 is a double root and $-1$ is a simple root, giving three roots total. Algebraically closed means no polynomial equation is left unsolvable inside the complex number system, even though many roots are non-real.

A useful consequence is the complex conjugate root theorem: if a real-coefficient polynomial has a non-real root $r$, then $\bar r$ is also a root, and $(z-r)(z-\bar r)$ is a real quadratic factor. Every real polynomial therefore splits into real linear and irreducible real quadratic factors, with the number of non-real roots always even. For example, $x^4 + a^4 = (x^2 + a\sqrt{2}\, x + a^2)(x^2 - a\sqrt{2}\, x + a^2)$, a factoring Leibniz wrongly claimed impossible in 1702 and Euler corrected in 1742.

The theorem is misnamed: it cannot be proved by algebra alone. Every known proof reaches outside the subject into analysis or topology, invoking tools like the intermediate value theorem, Liouville's theorem (a bounded entire function is constant), the winding number of a curve around the origin, or the maximum modulus principle. Argand gave the first rigorous proof in 1806; Gauss had given geometric proofs in 1799 and 1816 with gaps that Alexander Ostrowski filled only in 1920. Earlier partial attempts include d'Alembert (1746), Euler (1749), Lagrange (1772), and Laplace (1795).

A simple bound on where the roots can sit also follows: every root of a monic polynomial $z^n + a_{n-1}z^{n-1} + \cdots + a_0$ satisfies $|z| \le 1 + \max(|a_0|, \ldots, |a_{n-1}|)$. Combined with the theorem itself, that closed disk is guaranteed to contain at least one root, turning an abstract existence claim into a usable search region.

Since $\mathbb{C}$ is algebraically closed, it admits no proper finite field extension: any algebraic extension of the real field is isomorphic either to $\mathbb{R}$ itself or to $\mathbb{C}$, and every rational function with real coefficients has an elementary antiderivative expressed as a polynomial plus simple fractions over linear and irreducible quadratic denominators, because partial fractions can always be carried out over this complete factorisation.

Source: adapted from "Fundamental theorem of algebra" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Fundamental_theorem_of_algebra

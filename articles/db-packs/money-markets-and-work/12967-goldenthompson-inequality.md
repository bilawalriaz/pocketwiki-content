# Golden–Thompson inequality

The Golden–Thompson inequality is a trace inequality proved independently by Golden (1965) and Thompson (1965). It states that for Hermitian matrices $A$ and $B$,

$$\operatorname{tr} e^{A+B} \le \operatorname{tr}(e^A e^B).$$

Both sides are real. The right side is real because the cyclic property of the trace lets it be rewritten as $\operatorname{tr}(e^{A/2} e^B e^{A/2})$. Equivalently, in the Frobenius norm $\|\cdot\|$,

$$\|e^{A+B}\| \le \|e^A e^B\|.$$

## Why the inequality is needed

For real numbers, $e^{a+b} = e^a e^b$ exactly. The same identity holds when matrices $A$ and $B$ commute, because commuting exponentials multiply like scalars. Once $A$ and $B$ fail to commute, the equality collapses and $e^A e^B \ne e^{A+B}$. The Golden–Thompson inequality shows that the two quantities, though different, remain comparable. Petz (1994) proved equality holds if and only if $A$ and $B$ commute, so the gap measures non-commutativity.

## Proof sketch

**Golden inequality (1965).** For Hermitian positive semidefinite $A,B$ and any integer $n \ge 0$,

$$\operatorname{tr}\bigl((AB)^{2^n}\bigr) \le \operatorname{tr}\bigl((A^{2^1}B^{2^1})^{2^{n-1}}\bigr) \le \cdots \le \operatorname{tr}(A^{2^n} B^{2^n}).$$

The $n=0$ case is trivial. The $n=1$ step uses Cauchy–Schwarz together with $\operatorname{tr}(ABAB) = \|\sqrt{A}\, B \sqrt{A}\|^2 \ge 0$ to bound $\operatorname{tr}(ABAB)$ by $\operatorname{tr}(AABB)$. Higher $n$ follow by induction, applying Cauchy–Schwarz to sequences $a_k = (AB)^{2^{n-k}}(BA)^{2^{n-k}}$ and $b_k = (BA)^{2^{n-k}}(AB)^{2^{n-k}}$, whose trace powers are linked by cyclic permutations.

**Thompson (1965).** The Lie product formula gives

$$\operatorname{tr}(e^{A+B}) = \lim_{n\to\infty} \operatorname{tr}\bigl((e^{A/2^n} e^{B/2^n})^{2^n}\bigr),$$

and the Golden inequality bounds each term by $\operatorname{tr}(e^A e^B)$.

## Generalisations

*Unitarily invariant norms.* The same inequality holds in any unitarily invariant norm, not just the Frobenius (Bhatia 1997, Theorem IX.3.7), since these norms also satisfy Cauchy–Schwarz. In the Schatten $2^N$-norm, $\|e^{A+B}\|_{2^N} \le \|e^A e^B\|_{2^N}$ for any integer $N \ge 1$, and taking $N \to \infty$ recovers the operator-norm inequality $\|e^{A+B}\|_{op} \le \|e^A e^B\|_{op} = \|e^{A/2} e^B e^{A/2}\|_{op}$ (Tao 2010).

*Monotonicity of the matrix exponential.* A corollary (Tao 2010) is that $e^A \preceq e^B$ implies $A \preceq B$ for Hermitian $A,B$. The argument passes from $\langle e^A x, x\rangle \le \langle e^B x, x\rangle$ to $\|e^{A/2}x\| \le \|e^{B/2}x\|$, making $e^{-B/2} e^{A/2}$ a contraction, so $A-B$ has only non-positive eigenvalues.

*Three or more matrices.* The naive bound $\operatorname{tr}(e^{A+B+C}) \le |\operatorname{tr}(e^A e^B e^C)|$ is false. Lieb (1973) for three matrices and Sutter, Berta and Tomamichel (2016) for any number proved the correct extension

$$\operatorname{tr} e^{A+B+C} \le \operatorname{tr}(e^A \mathcal{T}_{e^{-B}} e^C),$$

where $\mathcal{T}_f(g) = \int_0^\infty (f+t)^{-1} g (f+t)^{-1}\, dt$ is the Fréchet derivative of the matrix logarithm. When $f$ and $g$ commute, $\mathcal{T}_f(g) = g f^{-1}$, and the three-matrix bound reduces to the original two-matrix inequality.

*Lie groups.* Bertram Kostant (1973) used the Kostant convexity theorem to lift the inequality from Hermitian matrices to all compact Lie groups.

Source: adapted from "Golden–Thompson inequality" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Golden%E2%80%93Thompson_inequality

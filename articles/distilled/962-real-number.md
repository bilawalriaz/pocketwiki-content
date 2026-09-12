# Real number

## Overview
A real number is a value that measures a continuous one-dimensional quantity (length, duration, temperature) and can be represented by an infinite decimal expansion. The set of real numbers, denoted $\mathbb{R}$, includes all rational numbers (integers and fractions) and irrational numbers (algebraic numbers like $\sqrt{2}$ and transcendental numbers like $\pi$). Real numbers form the unique Dedekind-complete ordered field: they support addition, multiplication, and a total order compatible with arithmetic, and every non-empty subset with an upper bound has a least upper bound (supremum). This completeness distinguishes $\mathbb{R}$ from the rationals and provides the rigorous foundation for calculus, analysis, and the modeling of physical quantities.

## Timeline
- **c. 1000 BC** — Egyptians use simple fractions.
- **c. 600 BC** — Vedic "Shulba Sutras" imply use of irrational numbers.
- **c. 500 BC** — Greek mathematicians (Pythagoreans) discover $\sqrt{2}$ is irrational.
- **c. 390–340 BC** — Eudoxus of Cnidus defines equality of irrational proportions (anticipating Dedekind cuts).
- **Middle Ages** — Indian, Chinese, and Arabic mathematicians accept zero, negatives, and fractions; Arabic mathematicians treat irrationals as algebraic objects.
- **16th century** — Simon Stevin establishes modern decimal notation; equates rational and irrational numbers in this regard.
- **17th century** — René Descartes coins "real" to distinguish roots of polynomials from "imaginary" numbers.
- **1761–1794** — Lambert and Legendre prove $\pi$ is irrational.
- **1840** — Liouville establishes existence of transcendental numbers.
- **1854** — Bernhard Riemann highlights need for rigorous definition of reals.
- **1858–1872** — Dedekind, Méray, Heine, and Cantor develop rigorous definitions (Dedekind cuts, Cauchy sequences).
- **1873** — Hermite proves $e$ is transcendental; Cantor proves reals are uncountable.
- **1882** — Lindemann proves $\pi$ is transcendental.
- **1963** — Paul Cohen proves Continuum Hypothesis independent of ZFC.

## Body

### Characterizing Properties
Real numbers are completely characterized as the unique (up to isomorphism) Dedekind-complete ordered field. This means they satisfy the field axioms (addition, multiplication, inverses, identities), are totally ordered (compatible with arithmetic), and possess **Dedekind completeness**: every non-empty subset with an upper bound has a least upper bound (supremum) in $\mathbb{R}$. This property fails for rational numbers (e.g., $\{x \in \mathbb{Q} : x^2 < 2\}$ has no least rational upper bound). Dedekind completeness implies the **Archimedean property** (for any real $x$, an integer $n > x$ exists), the existence of square roots for positive numbers, and that every odd-degree polynomial has a real root, making $\mathbb{R}$ a **real closed field**.

### Arithmetic and Order
$\mathbb{R}$ is an ordered field. Addition and multiplication are commutative, associative, and distributive. Identities $0$ (additive) and $1$ (multiplicative) exist; every element has an additive inverse $-a$, and every non-zero element has a multiplicative inverse $a^{-1}$. The total order $<$ satisfies trichotomy (exactly one of $a<b, a=b, b<a$ holds) and transitivity. Order is compatible with operations: $a<b \implies a+c<b+c$; $0<a \land 0<b \implies 0<ab$. Auxiliary operations (subtraction, division, absolute value $|a|=\max(a,-a)$) and relations ($\le, \ge, >$) are defined from these primitives. The natural numbers $\mathbb{N}$, integers $\mathbb{Z}$, and rationals $\mathbb{Q}$ embed into $\mathbb{R}$ as an ordered subfield via injective homomorphisms.

### Decimal Representation
A nonnegative real number corresponds to a decimal expansion $b_k \dots b_0 . a_1 a_2 \dots$ representing the series $\sum b_i 10^i + \sum a_j 10^{-j}$. Formally, the number is the least upper bound of the truncations $D_n$ (partial sums). This construction relies on the Archimedean property (to find the integer part) and Dedekind completeness (to ensure the supremum exists). Every real has at least one decimal representation; the mapping is bijective if representations ending in infinite trailing 9s are excluded. The same logic applies to any base $B \ge 2$.

### Topological Completeness
$\mathbb{R}$ is complete as a metric space (topological completeness). A **Cauchy sequence** $(x_n)$ satisfies: $\forall \varepsilon>0, \exists N, \forall m,n>N, |x_n-x_m|<\varepsilon$. A sequence **converges** to $x$ if $\forall \varepsilon>0, \exists N, \forall n>N, |x_n-x|<\varepsilon$. In $\mathbb{R}$, a sequence converges iff it is Cauchy. This equivalence fails in $\mathbb{Q}$ (e.g., decimal approximations of $\sqrt{2}$ are Cauchy but do not converge in $\mathbb{Q}$). Topological completeness underpins calculus: it allows proving a limit exists (e.g., for the exponential series $e^x = \sum x^n/n!$) by showing the sequence of partial sums is Cauchy, without computing the limit.

### "The Complete Ordered Field"
The phrase "the complete ordered field" admits three interpretations:
1.  **Lattice-complete**: Impossible for an ordered field (no largest element).
2.  **Dedekind-complete**: The sense used in the axiomatic definition; unique up to isomorphism. Related to construction via Dedekind cuts.
3.  **Uniformly complete**: $\mathbb{R}$ is the unique uniformly complete Archimedean field. Related to construction via Cauchy sequences (uniform completion of $\mathbb{Q}$).
David Hilbert originally used "complete Archimedean field" to mean the *largest* Archimedean field (every other is a subfield), related to the surreal numbers construction.

### Cardinality
The set $\mathbb{R}$ is **uncountable** (Cantor, 1874): no bijection exists with $\mathbb{N}$. Its cardinality is the **continuum**, denoted $\mathfrak{c}$ or $2^{\aleph_0}$, strictly greater than $\aleph_0$ (cardinality of $\mathbb{N}$). The **Continuum Hypothesis (CH)** states no cardinality lies strictly between $\aleph_0$ and $\mathfrak{c}$ (i.e., $\mathfrak{c} = \aleph_1$). CH is independent of ZFC (Cohen, 1963): it can be neither proved nor disproved from standard axioms.

### Other Properties
*   **Topology**: $\mathbb{R}$ is a separable, connected, simply connected, contractible, locally compact (but not compact) metric space of Hausdorff dimension 1. The metric topology ($|x-y|$) matches the order topology.
*   **Algebraic**: Every nonnegative real has a square root; no negative real does. Every odd-degree polynomial has a root. $\mathbb{R}$ is a real closed field.
*   **Measure**: The canonical Lebesgue measure (Haar measure normalized to unit interval) exists; non-measurable sets (e.g., Vitali sets) exist assuming Axiom of Choice.
*   **Logic**: The supremum axiom is second-order. First-order logic cannot characterize $\mathbb{R}$ uniquely (Löwenheim–Skolem); countable **nonstandard models** (e.g., hyperreals) satisfy the same first-order sentences, enabling nonstandard analysis.
*   **Vector Space**: $\mathbb{R}$ is a vector space over $\mathbb{Q}$. AC guarantees a basis (Hamel basis), but no explicit description exists.
*   **Well-ordering**: AC implies a well-ordering of $\mathbb{R}$ exists (standard order is not one), but it is not explicitly constructible.
*   **Computability**: A real is **computable** if an algorithm yields its digits. Only countably many reals are computable; equality of computable reals is undecidable.

### History
Early civilizations used fractions (Egypt) and encountered irrationals (Vedic India, Pythagorean Greece). Greeks treated numbers as proportions (ratios of lengths); Eudoxus defined equality of irrational proportions without arithmetic beyond multiplication by integers. The Middle Ages saw acceptance of zero, negatives, and algebra (Arabic mathematicians), merging "number" and "magnitude." Stevin (16th c.) systematized decimals. Descartes (17th c.) coined "real" vs. "imaginary." 18th–19th centuries resolved irrationality/transcendence of $\pi, e$ (Lambert, Legendre, Liouville, Hermite, Lindemann). The rigorization of analysis (Cauchy, Riemann) demanded formal definitions of $\mathbb{R}$, achieved independently in 1872 by Dedekind (cuts) and Cantor (Cauchy sequences). These relied on later foundations: Peano axioms for $\mathbb{N}$, Cantor's set theory for infinite sets, and higher-order logic for quantification over them. Cantor proved uncountability of $\mathbb{R}$ (1874) and countability of algebraic numbers.

### Formal Definitions
#### Axiomatic Approach
$\mathbb{R}$ is defined as a set with operations $+, \cdot$ and order $<$ satisfying:
1.  **Field**: Standard arithmetic axioms.
2.  **Ordered Field**: Total order $\ge$ compatible with $+$ and $\cdot$ ($x\ge y \implies x+z\ge y+z$; $x,y\ge0 \implies xy\ge0$).
3.  **Dedekind Complete**: Every nonempty subset with an upper bound has a least upper bound in $\mathbb{R}$.
These properties imply the Archimedean property and uniquely specify $\mathbb{R}$ up to unique isomorphism.

#### Construction from Rationals
$\mathbb{R}$ is constructed as a completion of $\mathbb{Q}$:
*   **Dedekind Cuts**: Partition $\mathbb{Q}$ into two nonempty sets $(A, B)$ where every element of $A$ is less than every element of $B$, and $A$ has no greatest element.
*   **Cauchy Sequences**: Equivalence classes of Cauchy sequences of rationals (two sequences equivalent if their difference tends to 0).
Both yield isomorphic Dedekind-complete ordered fields. Geometric constructions (Hilbert/Tarski axioms) are also equivalent.

### Applications and Connections
*   **Physics**: Physical constants and variables (position, mass, charge) are modeled as reals. Fundamental theories (classical mechanics, QM, GR, Standard Model) use structures (manifolds, Hilbert spaces) based on $\mathbb{R}$. Proposals for discrete foundations remain speculative.
*   **Logic**: Formalized in ZFC. Studied in reverse/constructive mathematics. **Hyperreals** (Robinson) extend $\mathbb{R}$ with infinitesimals for nonstandard analysis. **Internal Set Theory** (Nelson) treats infinitesimals as non-standard elements within $\mathbb{R}$.
*   **Computation**: Computers use finite-precision **floating-point** approximations (binary, ~16 decimal digits), which violate field axioms. **Numerical analysis** studies resulting errors. **Computer algebra systems** manipulate symbolic expressions (e.g., $\sqrt{2}, \int_0^1 x^x dx$) exactly, but face undecidability of equality and expression swell. **Computable reals** (algorithmically generated digits) are countable; most reals are uncomputable.
*   **Set Theory**: **Baire space** ($\mathbb{N}^\mathbb{N}$) serves as a surrogate for $\mathbb{R}$ in descriptive set theory to avoid connectedness complications.

### Generalizations and Extensions
*   **Complex numbers $\mathbb{C}$**: Algebraically closed, not ordered.
*   **Affinely extended reals $[-\infty, +\infty]$**: Compact, total order, complete lattice; not a field/group.
*   **Real projective line $\mathbb{R} \cup \{\infty\}$**: Compact, cyclic order; allows division by zero; not a field.
*   **Long real line**: Pastes $\aleph_1^* + \aleph_1$ copies of $\mathbb{R}$; largest complete, locally Archimedean ordered set; not a field.
*   **Hyperreal / Surreal numbers**: Non-Archimedean ordered fields containing infinitesimals and infinite numbers.
*   **Self-adjoint operators**: Generalize reals: ordered (not totally), complete, real eigenvalues, form real associative algebra. Positive-definite $\leftrightarrow$ positive reals; normal $\leftrightarrow$ complex numbers.

## Terms
- ****Dedekind completeness**** — Every non-empty subset of $\mathbb{R}$ with an upper bound has a least upper bound (supremum) in $\mathbb{R}$.
- ****Ordered field**** — A field with a total order compatible with addition and multiplication ($a<b \implies a+c<b+c$; $0<a,b \implies 0<ab$).
- ****Cauchy sequence**** — A sequence $(x_n)$ where terms become arbitrarily close: $\forall \varepsilon>0, \exists N, \forall m,n>N, |x_n-x_m|<\varepsilon$.
- ****Topological completeness**** — A metric space where every Cauchy sequence converges to a limit within the space.
- ****Real closed field**** — An ordered field where every positive element has a square root and every odd-degree polynomial has a root.
- ****Uncountable**** — An infinite set with no bijection to $\mathbb{N}$; cardinality strictly greater than $\aleph_0$.
- ****Continuum ($\mathfrak{c}$)**** — The cardinality of $\mathbb{R}$; equal to $2^{\aleph_0}$ (cardinality of the power set of $\mathbb{N}$).
- ****Continuum Hypothesis (CH)**** — The statement that no cardinality lies strictly between $\aleph_0$ and $\mathfrak{c}$ (i.e., $\mathfrak{c}=\aleph_1$).
- ****Computable number**** — A real number for which an algorithm exists to compute its digits to arbitrary precision.
- ****Nonstandard model**** — An ordered field satisfying the same first-order sentences as $\mathbb{R}$ but not isomorphic to it (e.g., hyperreals).

## Debates and open questions
*   **Continuum Hypothesis**: Independent of ZFC (Cohen, 1963); truth value depends on chosen set-theoretic axioms.
*   **Foundations of Analysis**: Debate between classical (ZFC), constructive (requiring computability/explicit witnesses), and nonstandard (infinitesimals) frameworks.
*   **Physical Reality of Continuum**: Whether spacetime is fundamentally continuous ($\mathbb{R}$-based) or discrete at the Planck scale remains an open question in quantum gravity.
*   **Explicit Hamel Basis**: AC proves $\mathbb{R}$ has a basis as a vector space over $\mathbb{Q}$, but no explicit construction is known (and may be impossible).
*   **Definability vs. Computability**: The hierarchy of "definable" (countable) vs. "computable" (countable) vs. arbitrary reals (uncountable) raises philosophical questions about the ontological status of "most" real numbers.

Source: adapted from "Real number" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Real_number

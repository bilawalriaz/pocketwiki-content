# Mathematical analysis

## Overview

Mathematical analysis is the branch of mathematics studying functions, spaces, and operators through approximation and convergence. Originating from 17th-century calculus, it was reformulated with rigor in the 19th century and remains central to scientific applications.

## Timeline

- **c. 300 BCE** — Eudoxus and Archimedes use method of exhaustion (limits, convergence)
- **433 BCE** — Ācārya Bhadrabāhu uses geometric series sum
- **3rd century CE** — Liu Hui applies exhaustion to circle area
- **14th century** — Oresme proves harmonic series divergence; Bradwardine on infinitesimals
- **1637** — Descartes publishes *La Géométrie* (analytic geometry)
- **1665–1675** — Newton and Leibniz develop infinitesimal calculus
- **1816** — Bolzano defines continuity (work not widely known until 1870s)
- **1821** — Cauchy begins rigorous calculus foundation
- **1870s** — Dedekind constructs reals via cuts; Weierstrass develops (ε,δ) limits
- **1900s–1920s** — Lebesgue integration; Hilbert spaces; Banach functional analysis

## Body

### Ancient and Medieval Foundations

Analysis traces to ancient Greek mathematics. Zeno's paradox implicitly involves infinite geometric sums, while Eudoxus and Archimedes used the method of exhaustion to compute areas and volumes, employing informal limit concepts. Archimedes' *Method of Mechanical Theorems* explicitly used infinitesimals. In Asia, Liu Hui (3rd century CE) applied exhaustion to circle area, and Hindu mathematicians knew arithmetic and geometric series formulas by 4th century BCE. Medieval Islamic mathematicians like Ibn al-Haytham worked on sums of powers and area problems, and Ibrahim ibn Sinan generalized Archimedean methods in the quadrature of the parabola. The Kerala school, especially Madhava, developed infinite series for trigonometric functions. Medieval European thinkers debated the continuum's nature: Aristotle distinguished potential vs. actual infinity; Bradwardine described continua as infinite infinitesimals; Occam held continua consist of points. Nicole Oresme gave a graphical proof of the mean speed theorem, representing displacement by the area under a velocity-time graph, and proved the divergence of the harmonic series. The works of Aristotle, which only became more widely available in Europe in the early 13th century, held that the continuum was not made of points. Richard Swineshead in *Liber calculationum* wrote that ratios involving infinity should simply be left undefined.

### Renaissance and the Birth of Calculus

The 17th century saw systematic anticipation of calculus. Kepler used infinitesimal arguments; Galileo connected math to motion; Cavalieri developed indivisibles; Torricelli extended geometric methods. Fermat's adequality found maxima/minima and tangents. Descartes' *La Géométrie* (1637) established analytic geometry. Newton and Leibniz independently created infinitesimal calculus, which evolved into analysis topics like calculus of variations, differential equations, and Fourier analysis.

### 19th-Century Rigorization

Euler introduced the modern function concept. Bolzano (1816) defined continuity, but his work did not become widely known until the 1870s. Cauchy (1821) rejected the "principle of the generality of algebra," formulating calculus via geometric ideas and infinitesimals, introducing Cauchy sequences and complex analysis. Weierstrass developed the (ε,δ)-definition of limit. Riemann advanced integration and complex analysis. Concern over unproven continuum assumptions led Dedekind to construct reals via cuts, filling rational "gaps." Pathological objects ("monsters") like nowhere-differentiable functions prompted Jordan's measure theory, Cantor's set theory, and Baire's category theorem. Lebesgue greatly improved measure theory and introduced his own theory of integration, which proved to be a big improvement over Riemann. Hilbert introduced Hilbert spaces to solve integral equations. The idea of normed vector space was in the air, and in the 1920s Banach created functional analysis.

### Core Concepts

**Real numbers**: Completeness (least-upper-bound property) underlies limits, continuity, differentiation, integration.

**Approximation and convergence**: Sequences converge to limits when terms stay within any ε-tolerance beyond some index N. Differentiability approximates functions linearly with error o(x−a). Taylor's theorem quantifies approximation error via second derivatives. Estimates (inequalities) bound approximation errors.

**Continuity**: Epsilon-delta definition ensures small input changes yield small output changes. Continuity enables local-to-global results: intermediate value property on intervals, maxima/minima on compact sets, uniform continuity on compact metric spaces.

**Metric spaces**: Sets with distance functions. Most analysis occurs here (real line, complex plane, Euclidean space). Banach and Hilbert spaces are complete normed spaces. Compactness equals sequential compactness in metric spaces, simplifying limit arguments.

**Complex variables**: Holomorphic functions (complex-differentiable) are analytic—locally representable by convergent power series. Contour integration, Cauchy integral theorem/formula, and residue theorem relate function values to boundary behavior and singularities.

**Measure theory**: Assigns sizes to sets via σ-algebras and countably additive measures. Lebesgue measure generalizes length/area/volume. Convergence almost everywhere (except measure-zero sets) replaces pointwise convergence. Lᵖ spaces consist of functions with integrable p-th powers.

**Function decomposition**: Fourier series decompose periodic functions into sinusoids (eigenfunctions of rotation group). Eigenfunction expansions exploit orthogonality in Hilbert spaces. Sobolev spaces link function smoothness to Fourier coefficient decay.

**Dynamics**: Differential equations model time evolution; iteration produces discrete dynamical systems. Questions include solution existence/uniqueness, stability, long-term behavior. Ergodic theory connects time averages to space averages. Operator semigroups generalize exponentials to infinite dimensions.

**Operators and spectral theory**: Differential, integral, and linear operators encode system evolution. Spectral theory decomposes operators analogously to eigenvalue decomposition in finite dimensions.

### Major Branches

Calculus studies derivatives (rates of change, linear approximation) and integrals (accumulation, area). Real analysis rigorously treats real functions and sequences. Complex analysis investigates holomorphic functions, useful in physics and number theory. Functional analysis studies vector spaces with limit structures and operators. Fourier analysis represents functions as wave superpositions. Harmonic analysis extends Fourier methods. Differential equations relate functions to derivatives. Measure theory assigns set sizes. Numerical analysis approximates solutions with error bounds. Geometric analysis applies calculus to manifolds. Convex analysis optimizes convex functions. Calculus of variations minimizes functionals. Probability theory uses measure-theoretic foundations.

### Applications

Analysis dominates classical mechanics, relativity, and quantum mechanics via differential equations (Newton's laws, Schrödinger equation, Einstein field equations). Signal processing uses Fourier transforms to isolate waveform components. Analysis also contributes to analytic number theory, combinatorics, differential geometry, topology, and information theory.

## Terms

- **Holomorphic function**: Complex-differentiable function, automatically analytic (locally power-series representable)
- **Metric space**: Set with distance function defining pairwise distances
- **σ-algebra**: Collection of sets closed under countable unions, intersections, complements
- **Lebesgue integral**: Integration theory based on measure, superior to Riemann for limits
- **Banach space**: Complete normed vector space
- **Hilbert space**: Complete inner product space
- **Eigenfunction expansion**: Decomposition into functions satisfying operator eigenvalue equations
- **Almost everywhere**: Property holding except on a set of measure zero
- **Spectral theory**: Study of operator decomposition generalizing eigenvalue analysis
- **Ergodic theory**: Study of measure-preserving transformations and time/space average equivalence

## Debates and Open Questions

Key historical debates included whether the continuum consists of points or infinitesimals (Aristotle, Occam, Bradwardine), and whether infinitesimals are legitimate (resolved by Weierstrass's ε-δ approach). The late 19th century grappled with unproven continuum assumptions, resolved by Dedekind's construction. Modern foundational debates persist in constructive vs. classical analysis, non-standard analysis (rigorous infinitesimals), and computable analysis (algorithmic computability).

Source: adapted from "Mathematical analysis" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Mathematical_analysis

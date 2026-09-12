# Mathematical analysis

Mathematical analysis is the branch of mathematics that studies functions, spaces, and operators through approximation and convergence. Where algebra asks for exact answers, analysis asks how answers can be approached, how close is close enough, and what happens in the limit. The subject grew out of 17th-century calculus, was rewritten with logical rigor in the 19th century, and supplies the working language of physics, engineering, and modern mathematics.

## Historical arc

Calculus was invented in the 1660s and 1670s by Newton and Leibniz, who used infinitesimals — quantities smaller than any positive number yet still nonzero — to compute rates of change and accumulated quantities. The earlier method of exhaustion, used by Eudoxus and Archimedes around 300 BCE to compute areas and volumes, sandwiched a shape between inscribed and circumscribed figures whose difference could be made arbitrarily small. In medieval Europe, Nicole Oresme proved that the harmonic series diverges, and Bradwardine described continua as built from infinitesimals.

The 19th century replaced these intuitive notions with a precise definition of limit, due largely to Cauchy (from 1821) and Weierstrass, who formalised the (ε, δ) statement: a sequence converges to a limit L if every tolerance ε > 0 can be matched by an index N beyond which all terms lie within ε of L. Bolzano had defined continuity in 1816, but his work circulated only from the 1870s. Because limits require no gaps in the number line, Dedekind constructed the real numbers from the rationals by cuts, filling the holes. In the early 20th century Lebesgue rebuilt integration on a general theory of measure, and Hilbert and Banach built the abstract spaces — Hilbert spaces and Banach spaces — that extend these ideas to functions and operators.

## Core ideas

**Real numbers and completeness.** The single most important property of the reals is completeness: every nonempty set bounded above has a least upper bound. Without it, Cauchy sequences of rationals can fail to settle on a rational limit; with it, they always settle on a real one.

**Approximation and convergence.** Many central theorems say that one object is well approximated by a simpler one, with explicit error bounds. Differentiability states that near a point a, a function is well approximated by its tangent line, with an error smaller than the step |x − a| as the step shrinks. Taylor's theorem quantifies the same idea one order higher, controlled by the next derivative. In every case, the practical content is the inequality bounding the error.

**Continuity.** A function is continuous at a point when small input changes produce small output changes, made precise by the same ε, δ language. Continuity on an interval buys the intermediate value theorem, and continuity on a compact set — a closed, bounded set in Euclidean space — buys the existence of a maximum and minimum, plus uniform continuity, in which a single δ works for every point.

**Metric and normed spaces.** A metric space is a set equipped with a notion of distance; the real line, the complex plane, and Euclidean space are metric spaces. A Banach space is a vector space complete with respect to a norm, and a Hilbert space is a Banach space whose norm comes from an inner product, so angles and orthogonal decompositions are available. In metric spaces, a set is compact if and only if every sequence in it has a convergent subsequence, which lets limit arguments be phrased in terms of sequences rather than coverings.

**Complex analysis.** A function of a complex variable that is differentiable once is automatically analytic, meaning it can be expanded locally as a convergent power series. This rigid structure produces contour integrals, the Cauchy integral theorem and formula, and the residue theorem, which compute integrals by reading off what happens at isolated singularities.

**Measure theory.** Measure theory assigns a size — length, area, volume, or probability — to sets via a σ-algebra, a collection closed under countable unions, intersections, and complements, together with a countably additive measure. The Lebesgue integral built on this foundation is more powerful than the Riemann integral, accommodating limits of functions the Riemann theory cannot handle, and lets one speak of a property holding almost everywhere, meaning everywhere except on a set of measure zero.

**Function decompositions.** Fourier series express periodic functions as sums of sines and cosines, the eigenfunctions of rotation. In a Hilbert space, any function can be expanded in an orthogonal basis of eigenfunctions of a suitable operator, and smoothness of the function corresponds to rapid decay of its Fourier coefficients, made precise by Sobolev spaces.

**Dynamics and operators.** Differential equations model how a system evolves in time; questions concern existence and uniqueness of solutions, stability, and long-term behaviour. Ergodic theory links long-time averages along a trajectory to averages over the whole space. Spectral theory extends the finite-dimensional idea of diagonalising a matrix to differential and integral operators on infinite-dimensional spaces.

## Major branches

Real analysis rigorously treats real-valued functions and sequences. Complex analysis investigates holomorphic functions, applied in physics and number theory. Functional analysis studies vector spaces with a limit structure together with the operators that act on them. Fourier and harmonic analysis decompose functions into waves. Differential equations tie functions to their own derivatives. Measure theory underlies probability and much of modern analysis. Numerical analysis builds algorithms with guaranteed error bounds. Geometric analysis applies calculus to curved spaces, and convex analysis with calculus of variations handles optimisation problems whose variables are functions or shapes.

## Applications

Differential equations encode the laws of classical mechanics, general relativity, and quantum mechanics. Fourier transforms isolate frequency components in signals, images, and audio. Measure-theoretic probability underpins modern statistics. Analysis also feeds analytic number theory, combinatorics, differential geometry, topology, and information theory.

## Continuing debates

Historical controversies about whether continua are built from points or from infinitesimals were settled, in mainstream mathematics, by the ε, δ framework and by Dedekind's construction of the reals. Active alternatives remain: constructive analysis insists that every existence proof supply an explicit example; non-standard analysis revives rigorous infinitesimals via an extended number system; and computable analysis restricts attention to functions an algorithm can actually carry out. These programmes change which objects are admitted as legitimate while leaving the core results of standard analysis intact.

Source: adapted from "Mathematical analysis" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Mathematical_analysis

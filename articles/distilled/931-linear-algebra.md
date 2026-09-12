# Linear algebra

## Overview

Linear algebra is the branch of mathematics concerning linear equations, linear maps, and their representations in vector spaces and through matrices. It is central to almost all areas of mathematics and is fundamental in modern geometry, functional analysis, and numerous scientific and engineering applications. Linear algebra provides tools for modeling natural phenomena and computing efficient solutions, including first-order approximations for nonlinear systems via differentials.

## Timeline

- **c. 150 BCE** — Gaussian elimination procedure appears in *The Nine Chapters on the Mathematical Art* (Chapter Eight: Rectangular Arrays)
- **1637** — René Descartes introduces Cartesian coordinates, linking geometry to linear equations
- **1693** — Gottfried Leibniz considers first systematic methods using determinants
- **1750** — Gabriel Cramer formulates Cramer's rule for explicit solutions of linear systems
- **1843** — William Rowan Hamilton discovers quaternions (H), introducing the term "vector"
- **1844** — Hermann Grassmann publishes *Theory of Extension*, foundational to modern linear algebra
- **1848** — James Joseph Sylvester introduces the term "matrix"
- **1856** — Arthur Cayley introduces matrix multiplication and inverse matrix
- **1872** — Benjamin Peirce publishes *Linear Associative Algebra*
- **1888** — Giuseppe Peano gives first modern definition of abstract vector space
- **1900** — Theory of linear transformations of finite-dimensional vector spaces emerges

## Body

### Vector Spaces

A vector space over a field F (typically real or complex numbers) is a set V with two operations: vector addition (v + w) and scalar multiplication (av), satisfying eight axioms that make V an abelian group under addition. Elements of V are vectors; elements of F are scalars. Vector spaces may contain tuples, sequences, functions, polynomials, or matrices. Linear algebra studies properties common to all vector spaces.

### Linear Maps

A linear map T: V → W between vector spaces preserves structure: T(u + v) = T(u) + T(v) and T(av) = aT(v). An equivalent condition is T(au + bv) = aT(u) + bT(v). When V = W, T is a linear operator. A bijective linear map is an isomorphism—preserving linear structure so isomorphic spaces are indistinguishable algebraically. Testing isomorphism, finding range and kernel (elements mapped to zero) are central problems solved via Gaussian elimination.

### Subspaces, Span, and Basis

A linear subspace W of V is closed under addition and scalar multiplication. The span of a set S is all linear combinations of S's elements—the smallest subspace containing S. Vectors are linearly independent if none lies in the span of others. A basis is a linearly independent spanning set. All bases of a vector space have the same cardinality (dimension theorem). Finite-dimensional spaces have finite bases; subspaces satisfy dim U ≤ dim V.

### Matrices

Matrices enable explicit manipulation of finite-dimensional vector spaces and linear maps. Given basis (v₁,...,vₘ) of V, coordinates (a₁,...,aₘ) form an isomorphism Fᵐ → V. Linear maps f: W → V correspond to matrices whose columns are f(wⱼ) expressed in V's basis. Matrix multiplication mirrors composition of linear maps. Similar matrices represent the same transformation in different bases, connected by elementary row/column operations. Gaussian elimination finds these transformations.

### Linear Systems

A system Ax = b of m linear equations in n variables associates with matrix A and vectors x, b. Solutions are preimages under the linear transformation T. The homogeneous system Ax = 0 has solutions forming the kernel of T. Gaussian elimination on the augmented matrix [A|b] produces reduced row echelon form without changing solutions. If m = n and A is invertible, the unique solution is x = A⁻¹b.

### Endomorphisms and Square Matrices

A linear endomorphism maps V to itself, represented by square matrices when a basis is chosen. These are central to geometric transformations, coordinate changes, and quadratic forms.

### Determinant

The determinant of square matrix A is Σ_{σ∈Sₙ} (-1)^σ a₁σ(₁)⋯aₙσ(ₙ), summing over all permutations. A matrix is invertible iff its determinant is nonzero. Cramer's rule gives closed-form solutions via determinants but is computationally inefficient for large n. The determinant of an endomorphism is basis-independent.

### Eigenvalues and Eigenvectors

For endomorphism f, an eigenvector v satisfies f(v) = av (eigenvalue a). In matrix form: Mz = az, rewritten as (M - aI)z = 0. Eigenvalues are roots of the characteristic polynomial det(xI - M), a monic degree-n polynomial with at most n roots. Diagonalizable maps have bases of eigenvectors yielding diagonal matrices. Non-diagonalizable matrices exist (e.g., [[0,1],[0,0]]). Jordan and Frobenius normal forms handle non-diagonalizable cases.

### Duality

A linear form maps V → F. The dual space V* contains all linear forms. For basis (v₁,...,vₙ) of V, dual basis (v₁*,...,vₙ*) satisfies vᵢ*(vⱼ) = δᵢⱼ. The double dual V** is canonically isomorphic to V when finite-dimensional. The dual map f*: W* → V* satisfies (f*(h))(v) = h(f(v)); its matrix is the transpose of f's matrix.

### Inner-Product Spaces

An inner product ⟨·,·⟩: V×V → F satisfies conjugate symmetry, linearity in first argument, and positive-definiteness. It defines length ||v||² = ⟨v,v⟩ and angle via Cauchy-Schwarz inequality. Orthogonal vectors satisfy ⟨u,v⟩ = 0. Orthonormal bases (unit, mutually orthogonal vectors) simplify computations via Gram-Schmidt. Normal matrices (TT* = T*T) have orthonormal eigenvector systems.

### Geometry and Applications

Linear algebra originated with Descartes' 1637 Cartesian coordinates, representing lines/planes as linear equations. Geometric transformations (rotations, reflections, projections) are linear maps. Modern geometry is built on vector spaces. Applications span functional analysis (quantum mechanics, Fourier analysis), scientific computation (BLAS, LAPACK libraries), ambient space modeling (robotics, computer graphics), complex systems (linearized PDEs, weather forecasting), and engineering (fluid dynamics, power systems).

## Terms

- **Vector space**: Set with vector addition and scalar multiplication satisfying eight axioms
- **Linear map**: Function preserving vector addition and scalar multiplication
- **Basis**: Linearly independent set spanning the entire space
- **Determinant**: Scalar value encoding matrix invertibility and geometric scaling
- **Eigenvalue/eigenvector**: Scalar/vector where f(v) = av
- **Dual space (V*)**: Space of all linear forms on V
- **Inner product**: Bilinear/sesquilinear form defining length and angle
- **Isomorphism**: Bijective linear map preserving structure
- **Kernel**: Set of vectors mapped to zero
- **Span**: All linear combinations of a set of vectors

## Debates and Open Questions

The source notes that 19th-century mathematicians developed linear algebra's core results without defining abstract vector spaces, raising questions about whether abstraction was necessary for progress. The relationship between synthetic geometry (axiom-based) and analytic geometry (vector space-based) was historically debated but is now considered equivalent. The choice between matrix-based and vector-space-based presentations remains pedagogically contested, with vector spaces being more general but more abstract.

Source: adapted from "Linear algebra" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Linear_algebra

# Linear algebra

Linear algebra is the branch of mathematics that studies linear equations, linear maps (functions preserving addition and scaling), and their representation through vector spaces and matrices. It supplies the working language of modern geometry, functional analysis, and most scientific and engineering computation, including the first-order approximations that linearize nonlinear systems.

## Vector spaces, subspaces, and bases

A vector space over a field F (usually the real or complex numbers) is a set V with two operations: vector addition and scalar multiplication. The eight axioms that govern them are exactly the axioms of an abelian group under addition plus a compatible scaling action by F. Elements of V are vectors and elements of F are scalars, but the labels are broad: tuples, sequences, functions, polynomials, and matrices can all act as vectors once the operations are defined.

A linear subspace is a subset of V closed under both operations. The span of a set S of vectors is the smallest subspace containing S, built from all finite linear combinations of elements of S. A set is linearly independent when no member is a linear combination of the others. A basis is a linearly independent set whose span is the whole space, and the dimension theorem says every basis of a given space has the same cardinality.

## Linear maps

A linear map T: V → W between vector spaces satisfies T(u + v) = T(u) + T(v) and T(av) = aT(v), equivalently T(au + bv) = aT(u) + bT(v). When V = W, T is a linear operator. A bijective linear map is an isomorphism: it preserves the full linear structure, so V and W are indistinguishable by any linear-algebraic test. Three central problems are whether a map is an isomorphism, what its range is, and what its kernel is, the vectors that map to zero. Gaussian elimination answers all three at once.

## Matrices and linear systems

Fixing a basis turns every vector into a coordinate tuple and every linear map into a matrix. Matrix multiplication mirrors composition of maps, and a matrix is invertible precisely when its map is bijective. Similar matrices encode the same map in different bases and are connected by the elementary row and column operations that drive Gaussian elimination.

A linear system Ax = b asks which vector x the map represented by A sends to b. Row-reducing the augmented matrix [A | b] preserves the solution set, and when A is square and invertible the unique solution is x = A⁻¹b. The determinant of a square matrix records geometric scaling and invertibility: A is invertible if and only if det A ≠ 0. Cramer's rule expresses the answer in terms of determinants but is inefficient for large systems, so Gaussian elimination remains the practical workhorse.

## Endomorphisms, eigenvalues, and normal forms

A linear endomorphism maps V to itself and is represented by a square matrix once a basis is chosen. An eigenvector v of an endomorphism f satisfies f(v) = av for some scalar a, the eigenvalue. In matrix form Mz = az, or (M − aI)z = 0, the eigenvalues are the roots of the characteristic polynomial det(xI − M), a monic polynomial of degree n with at most n roots. When a basis of eigenvectors exists, the matrix becomes diagonal, the simplest possible form. Not every matrix diagonalizes; the 2×2 matrix [[0, 1], [0, 0]] is a standard counterexample. The Jordan and Frobenius normal forms handle the non-diagonalizable case.

## Duality and inner products

A linear form is a map V → F, and the dual space V* is the space of all such forms. Given a basis (v₁, …, vₙ), the dual basis (v₁*, …, vₙ*) satisfies vᵢ*(vⱼ) = δᵢⱼ, and for finite-dimensional V the double dual V** is canonically isomorphic to V. A map f: V → W induces a dual map f*: W* → V* whose matrix is the transpose of f's matrix.

An inner product ⟨·,·⟩ is conjugate-symmetric, linear in its first argument, and positive-definite. It defines length by ||v||² = ⟨v, v⟩ and angle through the Cauchy–Schwarz inequality. Vectors with ⟨u, v⟩ = 0 are orthogonal. Gram–Schmidt builds an orthonormal basis (unit vectors, mutually orthogonal) from any basis, and normal matrices satisfying TT* = T*T are precisely those with an orthonormal basis of eigenvectors.

## Applications

Geometric transformations (rotations, reflections, projections) are linear maps, and modern geometry is built on vector spaces. Functional analysis, quantum mechanics, and Fourier analysis rest on the same foundations. The BLAS and LAPACK libraries form the standard computational backbone. Robotics and computer graphics model three-dimensional space as a vector space. Weather forecasting and fluid dynamics rely on linearized partial differential equations, and power-systems engineering uses these tools to model large linear networks.

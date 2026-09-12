# Kernel (linear algebra)

A *linear map* L sends vectors from one space to another while preserving addition and scalar multiplication. The **kernel** (also called the **null space**) of L is the set of every input vector that L sends to the zero vector. Formally, if L : V → W, then

> ker(L) = { v ∈ V : L(v) = 0 } = L⁻¹(0).

The kernel is always a *linear subspace* of the domain V: it contains the zero vector and is closed under addition and scalar multiplication.

## What the kernel detects

Two inputs have the same output under L if and only if their difference lies in the kernel, because L(v₁) = L(v₂) is equivalent to L(v₁ − v₂) = 0. So the kernel records which distinct inputs L identifies with each other.

This connects the kernel to the *image* (the set of all outputs) through the first isomorphism theorem, im(L) ≅ V / ker(L). In finite dimensions this becomes the **rank–nullity theorem**:

> dim(ker L) + dim(im L) = dim(V).

Here *rank* means the dimension of the image and *nullity* means the dimension of the kernel, so a map cannot simultaneously have a large image and a large kernel.

## Kernels of matrices

When L is represented by an m×n matrix A over a field K (usually ℝ or ℂ), the kernel is the solution set of Ax = 0, a *homogeneous* linear system. Its dimension is the nullity of A, and rank(A) + nullity(A) = n.

The i-th component of Ax equals the *dot product* of the i-th row of A with x, so Ax = 0 says exactly that x is *orthogonal* to every row. The *row space* of A is the span of its rows; the kernel is the **orthogonal complement** of the row space, and dim(row space) = rank(A). The kernel, row space, column space, and left null space of A are the four fundamental subspaces associated with the matrix.

## Worked example

Take A = [[2, 3, 5], [−4, 2, 3]]. Solving Ax = 0:

> 2x + 3y + 5z = 0
> −4x + 2y + 3z = 0

Gauss–Jordan elimination reduces this to x = −z/16, y = −13z/8, giving the parametric form

> (x, y, z) = c · (−1, −26, 16).

The kernel is a line through the origin in ℝ³, spanned by a single vector, so nullity = 1. With rank 2 and n = 3, rank + nullity = 3, confirming rank–nullity. Dot products with both rows vanish: [2, 3, 5]·(−1, −26, 16) = 0 and [−4, 2, 3]·(−1, −26, 16) = 0, confirming orthogonality to the row space.

## Other kernels

- Evaluation L(f) = f(0.3) on continuous functions has kernel equal to all continuous functions vanishing at 0.3.
- The differentiation operator D(f) = df/dx has kernel equal to the constant functions, since these are precisely the functions whose derivative is zero.
- The shift operator s(x₁, x₂, x₃, …) = (x₂, x₃, x₄, …) has kernel (x₁, 0, 0, 0, …), a one-dimensional subspace.

The idea extends to homomorphisms of modules (generalised vector spaces where scalars come from a ring rather than a field), where the kernel is a submodule, though rank and nullity need not apply.

## Computation

A basis for the kernel of A is computed by stacking the identity below A to form [A | I], reducing by Gaussian elimination to column echelon form, and reading off the columns of the lower block that align with zero columns of the upper block. A nonhomogeneous system Ax = b has a solution exactly when b lies in the column space of A; whenever solutions exist, any two differ by an element of the kernel, so the full solution set is {v + x : Av = b, x ∈ ker(A)}, a translate of the kernel.

Source: adapted from "Kernel (linear algebra)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Kernel_%28linear_algebra%29

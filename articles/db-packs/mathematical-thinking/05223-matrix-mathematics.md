# Matrix (mathematics)

A matrix is a rectangular grid of numbers arranged in rows and columns, written inside brackets or parentheses. A grid with *m* rows and *n* columns is an *m* × *n* matrix, read "m by n." The 2 × 3 matrix [[1, 9, −13], [20, 5, −6]] has two rows and three columns. The numbers inside are entries or elements, and the entry in row *i*, column *j* is written *a*ᵢⱼ. Matrices are named with capital letters (**A**, **B**) and their entries with lowercase letters and two subscripts. Mathematical writing counts rows and columns starting at 1; most programming languages start at 0.

## Basic operations

**Addition** is entry by entry and requires identical size: (**A** + **B**)ᵢⱼ = *a*ᵢⱼ + *b*ᵢⱼ. **Scalar multiplication** multiplies every entry by a number *c*: (*c***A**)ᵢⱼ = *c* · *a*ᵢⱼ, so subtraction is **A** + (−1)**B**.

**Transpose** flips rows and columns: (**A**ᵀ)ᵢⱼ = *a*ⱼᵢ, turning an *m* × *n* matrix into an *n* × *m* one, and (**A**ᵀ)ᵀ = **A**.

**Matrix multiplication** is the operation that makes matrices useful. The product **AB** is defined only when the number of columns in **A** equals the number of rows in **B**; if **A** is *m* × *n* and **B** is *n* × *p*, the result is *m* × *p*, with each entry a sum of products:

(**AB**)ᵢⱼ = ∑ᵣ *a*ᵢᵣ *b*ᵣⱼ

That entry is the dot product of row *i* of **A** with column *j* of **B**. Multiplication is associative, (**AB**)**C** = **A**(**BC**), and distributes over addition, but is not commutative: **AB** ≠ **BA** in general, and the two products may not both be defined. Order matters.

## Linear systems

A system of linear equations becomes **Ax** = **b**, where **A** holds the coefficients, **x** is a column vector of unknowns, and **b** is a column vector of constants. If **A** is square and invertible, the solution is **x** = **A**⁻¹**b**. Row operations, which add a multiple of one row to another, scale a row by a nonzero constant, or swap two rows, drive Gaussian elimination, the standard algorithm for solving linear systems and finding inverses.

## Linear transformations

An *m* × *n* matrix **A** encodes a linear map from *n*-dimensional space to *m*-dimensional space: it sends a vector **x** to **Ax**. Every linear transformation between finite-dimensional spaces corresponds to a matrix once bases are chosen, and matrix multiplication corresponds to composing transformations. A 2 × 2 matrix [[*a*, *c*], [*b*, *d*]] sends the unit square to a parallelogram with vertices (0,0), (*a*,*b*), (*a*+*c*, *b*+*d*), (*c*,*d*).

## Square matrices

A square matrix has the same number of rows and columns. Several properties are defined only for square matrices.

- **Main diagonal:** the entries *a*₁₁, *a*₂₂, …, *a*ₙₙ from top-left to bottom-right.
- **Diagonal, upper-triangular, lower-triangular:** nonzero entries restricted to the diagonal, below it, or above it.
- **Identity matrix Iₙ:** 1s on the diagonal, 0s elsewhere, and **AI**ₙ = **I**ₘ**A** = **A**.
- **Symmetric:** **A** = **A**ᵀ. **Skew-symmetric:** **A** = −**A**ᵀ. The complex analog is the **Hermitian** matrix, defined by **A**\* = **A**, where the star denotes the conjugate transpose.
- **Invertible (non-singular):** there exists **B** with **AB** = **BA** = **I**ₙ. The inverse **A**⁻¹ is unique, and a square matrix is invertible if and only if its determinant is nonzero.
- **Orthogonal:** a real square matrix with orthonormal rows and columns, equivalently **A**ᵀ = **A**⁻¹. Its determinant is +1 (pure rotation) or −1 (rotation combined with reflection).
- **Positive-definite:** a symmetric real matrix **A** for which **x**ᵀ**A****x** > 0 for every nonzero vector **x**, which holds if and only if all eigenvalues are positive.

The **determinant** det(**A**) is a single number that encodes how the map scales areas (in 2D) or volumes (in 3D), and its sign records whether orientation is preserved. For a 2 × 2 matrix, det [[*a*, *b*], [*c*, *d*]] = *ad* − *bc*. Determinants multiply: det(**AB**) = det(**A**) · det(**B**).

**Eigenvalues and eigenvectors** are scalars λ and nonzero vectors **v** with **Av** = λ**v**. The eigenvalues are the roots of the characteristic polynomial det(λ**I** − **A**) = 0, a polynomial of degree *n*, so an *n* × *n* matrix has at most *n* eigenvalues, possibly complex or repeated. By the Cayley–Hamilton theorem, a matrix satisfies its own characteristic polynomial.

## Decomposition

Large computations become tractable by factoring matrices into simpler pieces. **LU decomposition** writes **A** = **LU**, lower-triangular times upper-triangular, which makes solving linear systems cheap. **Eigendecomposition** writes **A** = **VDV**⁻¹ with **D** diagonal when **A** is diagonalizable, so **A**ⁿ = **VD**ⁿ**V**⁻¹ reduces exponentiation to powering a diagonal matrix. **Singular value decomposition (SVD)** factors any matrix **A** = **U D V**\*, with **U** and **V** unitary and **D** diagonal, and is the standard tool for low-rank approximation and principal component analysis.

## Computational considerations

Multiplying two *n* × *n* matrices by the definition costs *n*³ scalar multiplications. Strassen's algorithm reduces this to roughly *n*²·⁸⁰⁷; further theoretical speedups exist but are rarely practical. *Sparse* matrices, in which most entries are zero, allow far more efficient specialised algorithms. Numerical stability matters: dividing by a near-zero determinant to compute an inverse produces large rounding errors, and matrix norms quantify how ill-conditioned a problem is.

## Generalizations

Entries can come from any field, including finite fields used in coding theory, or from any ring. Block matrices treat other matrices as entries. Tensors generalise the rectangular grid to higher dimensions. The set of *n* × *n* matrices over a ring *R* forms a *matrix ring* M(*n*, *R*). The collection of all invertible *n* × *n* matrices is the *general linear group* GL(*n*); properties preserved under multiplication and inversion carve out subgroups such as the *special linear group* (determinant 1) and the *orthogonal group* (**A**ᵀ**A** = **I**). Every finite group is isomorphic to some matrix group.

Source: adapted from "Matrix (mathematics)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Matrix_%28mathematics%29

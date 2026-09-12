# Minor (linear algebra)

In linear algebra, a **minor** of a matrix *A* is the determinant of a smaller square matrix cut out of *A* by deleting selected rows and columns. A **first minor** Mᵢⱼ is the determinant of the submatrix that remains after removing row *i* and column *j*. The **cofactor** Cᵢⱼ is that minor multiplied by (−1)^(i+j), which attaches a + or − sign depending on the parity of the row-plus-column index. Cofactors are also the partial derivatives of the determinant function with respect to each matrix entry.

## A worked example

Take the 3×3 matrix

$$
\begin{bmatrix} 1 & 4 & 7 \\ 3 & 0 & 5 \\ -1 & 9 & 11 \end{bmatrix}
$$

The minor M₂,₃ is the determinant after deleting row 2 and column 3:

$$
\det\begin{bmatrix} 1 & 4 \\ -1 & 9 \end{bmatrix} = 9 - (-4) = 13
$$

The cofactor is C₂,₃ = (−1)^(2+3) · 13 = −13.

## General k×k minors

For an *m*×*n* matrix *A* and 0 < *k* ≤ min(*m*, *n*), a *k*×*k* minor is the determinant of a *k*×*k* submatrix obtained by deleting *m*−*k* rows and *n*−*k* columns. The minor of order zero is defined to be 1; for a square matrix, the zeroth minor is the determinant of the whole matrix. The number of distinct *k*×*k* minors is

$$
\binom{m}{k} \cdot \binom{n}{k}
$$

because any *k* rows and *k* columns can be chosen independently. Different authors use different notations for the minor indexed by row set *I* and column set *J*: det_{I,J} A, [A]_{I,J}, or M_{I,J}. Some define it by selecting rows *I* and columns *J*; others define it by deleting them; for first minors Mᵢⱼ the deletion meaning is universal.

The **complement** of a minor of a square matrix is the determinant of what remains after removing the rows and columns used by that minor. The complement of a first minor of entry aᵢⱼ is aᵢⱼ itself.

## Cofactor expansion

Expanding along the *j*-th column gives Laplace's formula:

$$
\det(A) = \sum_{i=1}^{n} a_{ij}(-1)^{i+j}M_{ij}
$$

Expanding along the *i*-th row works the same way. This reduces an *n*×*n* determinant to *n* smaller (*n*−1)×(*n*−1) determinants, which makes first minors computationally useful.

## Matrix inverse

Arranging every cofactor of an *n*×*n* matrix *A* into a matrix **C** (the cofactor matrix, or comatrix) gives the **adjugate** (classical adjoint) as **C**ᵀ. The inverse is

$$
A^{-1} = \frac{1}{\det(A)} C^{T}
$$

which holds whenever det(A) ≠ 0. A more general identity expresses any *k*×*k* submatrix of A⁻¹ using complementary minors of *A*:

$$
[A^{-1}]_{I,J} = \pm \frac{[A]_{J', I'}}{\det A}
$$

where *I*′ and *J*′ are the complementary index sets, and the sign is (−1)^(Σiₛ − Σjₛ).

## Rank and principal minors

If *A* is an *i*×*j* matrix over a field with rank *r*, then at least one *r*×*r* minor is nonzero and every larger minor is zero. The size of the largest nonzero square subdeterminant equals the rank.

Three related notions differ in which index sets are used:
- **Principal minor**: choose the same set *I* for rows and columns, [A]_{I,I}.
- **Leading principal minor**: choose the first *m* rows and first *m* columns, [A]_{{1,…,m},{1,…,m}}.
- **Basic minor**: an *r*×*r* minor of nonzero value when the matrix has rank *r*.

For Hermitian matrices, all leading principal minors being positive is equivalent to positive definiteness (Sylvester's criterion); all principal minors being nonnegative characterizes positive semidefiniteness.

## Minors of a product

The minors of a product follow a generalized multiplication rule. For *A* of size *i*×*k*, *B* of size *k*×*j*, and index sets *I* ⊂ {1,…,*i*}, *J* ⊂ {1,…,*j*} each of size *m*:

$$
[AB]_{I,J} = \sum_{K} [A]_{I,K} [B]_{K,J}
$$

where *K* ranges over all *m*-element subsets of {1,…,*k*}. Ordinary matrix multiplication is the case *m* = 1, and the Cauchy–Binet formula for det(AB) (when applicable) is the square case *i* = *j* = *m*.

## Multilinear algebra viewpoint

Wedging *k* columns of *A* together produces a *k*-vector whose components are exactly the *k*×*k* minors. For the matrix

$$
\begin{pmatrix} 1 & 4 \\ 3 & -1 \\ 2 & 1 \end{pmatrix}
$$

wedging its two columns gives −13 e₁∧e₂ − 7 e₁∧e₃ + 5 e₂∧e₃, whose coefficients match the three 2×2 minors −13, −7, and 5. The *k*-minors of a matrix are the entries of the *k*-th exterior power map, which is why they appear in volume and orientation computations.

## A note on terminology

Some older books call a cofactor an **adjunct**, written Aᵢⱼ = (−1)^(i+j) Mᵢⱼ. The **adjugate** (transpose of the cofactor matrix) and the **adjoint** (usually a linear-operator concept) are different things and should not be confused with adjunct.

Source: adapted from "Minor (linear algebra)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Minor_%28linear_algebra%29

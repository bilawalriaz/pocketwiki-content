# Trace (linear algebra)

The trace of a square matrix $A$ is the sum of its main diagonal entries: $\operatorname{tr}(A) = \sum_{i=1}^n a_{ii} = a_{11} + a_{22} + \cdots + a_{nn}$. It is defined only for $n \times n$ matrices, with entries that may be real, complex, or elements of a field.

For example, if $A = \begin{pmatrix} 1 & 0 & 3 \\ 11 & 5 & 2 \\ 6 & 12 & -5 \end{pmatrix}$, then $\operatorname{tr}(A) = 1 + 5 + (-5) = 1$.

## Basic properties

The trace is linear: $\operatorname{tr}(A + B) = \operatorname{tr}(A) + \operatorname{tr}(B)$ and $\operatorname{tr}(cA) = c\operatorname{tr}(A)$. A matrix and its transpose share a diagonal, so $\operatorname{tr}(A) = \operatorname{tr}(A^{\mathsf{T}})$.

## Trace of a product

The central identity is the cyclic property. If $A$ is $m \times n$ and $B$ is $n \times m$, then $\operatorname{tr}(AB) = \operatorname{tr}(BA)$, proved by expanding $\operatorname{tr}(AB) = \sum_{i,j} a_{ij}b_{ji}$ and swapping summation. Note $AB \neq BA$ in general, yet their traces match, and neither equals $\operatorname{tr}(A)\operatorname{tr}(B)$.

The rule extends to cyclic permutations: $\operatorname{tr}(ABC) = \operatorname{tr}(BCA) = \operatorname{tr}(CAB)$. Arbitrary reorderings are not allowed, except for products of three symmetric matrices, where $\operatorname{tr}(ABC) = \operatorname{tr}(ACB)$ follows from $\operatorname{tr}(M) = \operatorname{tr}(M^{\mathsf{T}})$.

Similarity invariance follows: $\operatorname{tr}(P^{-1}AP) = \operatorname{tr}(A)$ for any invertible $P$. This makes the trace basis-independent, so it is defined for any linear operator on a finite-dimensional vector space, since all matrix representations of the same operator are similar.

## Trace of special matrices

| Matrix | Trace |
|---|---|
| Identity $I_n$ | $n$ |
| Hermitian | real (diagonal entries are real) |
| Permutation matrix | number of fixed points |
| Orthogonal projection | rank of the projected subspace |
| Idempotent ($A^2 = A$) | $\operatorname{rank}(A)$ |
| Nilpotent | $0$ |

Over a field of characteristic zero, the converse holds: if $\operatorname{tr}(A^k) = 0$ for all $k$, then $A$ is nilpotent. In positive characteristic $n$, $I_n$ gives a counterexample, since $\operatorname{tr}(I_n^k) = n \equiv 0$ yet $I_n$ is not nilpotent.

## Sum of eigenvalues

Every $n \times n$ matrix satisfies $\operatorname{tr}(A) = \sum_{i=1}^n \lambda_i$, where the $\lambda_i$ are eigenvalues counted with algebraic multiplicity. This holds even for real $A$ with complex eigenvalues, or over any field using eigenvalues from an algebraic closure. The identity follows because $A$ is similar to its Jordan form, an upper triangular matrix with $\lambda_i$ on its diagonal, combined with similarity invariance. The determinant plays the multiplicative analogue: $\det(A) = \prod_i \lambda_i$. The trace is also the coefficient of $t^{n-1}$ in the characteristic polynomial, up to sign.

## Trace of a commutator

If $[A, B] = AB - BA$, then $\operatorname{tr}([A, B]) = 0$ by linearity and $\operatorname{tr}(AB) = \operatorname{tr}(BA)$. The kernel of $\operatorname{tr}: \mathfrak{gl}_n \to k$ consists of the traceless matrices, forming the simple Lie algebra $\mathfrak{sl}_n$, which splits as $\mathfrak{gl}_n = \mathfrak{sl}_n \oplus k$ via the projection $A \mapsto \tfrac{1}{n}\operatorname{tr}(A)\,I$. The identity matrix is never similar to a commutator because it has nonzero trace.

## Derivative and determinant

For small entries, $\det(I + a) \approx 1 + \operatorname{tr}(a)$; precisely, the trace is the derivative of the determinant at the identity. Jacobi's formula generalises this: $d\det(A) = \operatorname{tr}(\operatorname{adj}(A) \cdot dA)$. A consequence is $\det(\exp(A)) = \exp(\operatorname{tr}(A))$. Interpreting $A$ as a linear vector field $F(x) = Ax$, the divergence of $F$ equals $\operatorname{tr}(A)$.

## Inner product structure

For real $m \times n$ matrices, $\operatorname{tr}(A^{\mathsf{T}}B) = \sum_{i,j} a_{ij} b_{ij}$. This is the Frobenius inner product, a positive-definite symmetric bilinear form with $\operatorname{tr}(A^{\mathsf{T}}A) = 0$ if and only if $A = 0$. The associated Frobenius norm satisfies $0 \leq [\operatorname{tr}(AB)]^2 \leq \operatorname{tr}(A^{\mathsf{T}}A)\operatorname{tr}(B^{\mathsf{T}}B)$. For complex matrices, replacing the transpose with the conjugate gives a Hermitian inner product. For column vectors, $\operatorname{tr}(ba^{\mathsf{T}}) = a^{\mathsf{T}}b$.

## Characterisation

Any linear functional $f$ on $n \times n$ matrices satisfying $f(XY) = f(YX)$ is a scalar multiple of the trace. Normalising $f(I) = n$ fixes the scalar and recovers $\operatorname{tr}$ exactly.

## Generalisations

On a Hilbert space, the trace extends to trace-class compact operators via $\operatorname{tr}(K) = \sum_n \langle e_n, K e_n \rangle$ for any orthonormal basis, with the Hilbert–Schmidt norm playing the role of the Frobenius norm. The partial trace handles operators on tensor product spaces: $\operatorname{tr}_A(\operatorname{tr}_B(Z)) = \operatorname{tr}_B(\operatorname{tr}_A(Z)) = \operatorname{tr}(Z)$. Stochastic estimation uses Hutchinson's trick: for random $u$ with $\mathbb{E}[uu^{\intercal}] = I$, $\mathbb{E}[u^{\intercal}Wu] = \operatorname{tr}(W)$.

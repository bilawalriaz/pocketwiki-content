# Rank (linear algebra)

The rank of a matrix is the number of linearly independent columns it contains, and equally the dimension of the vector space spanned by those columns. Rank measures the amount of independent information a matrix carries: it determines whether a system of linear equations has no solution, one solution, or infinitely many, and whether the corresponding linear transformation is reversible.

## Column rank equals row rank

A matrix has a column space, the span of its columns, and a row space, the span of its rows. Each has a dimension. A central result in linear algebra is that these two dimensions are always equal, so a single number, the rank, describes both. Two other equivalent characterisations follow directly: the rank of a matrix is the maximal number of linearly independent columns, and also the maximal number of linearly independent rows.

The standard proof uses row reduction. Elementary row operations swap rows, multiply a row by a nonzero scalar, or add a multiple of one row to another. None of these change the row space, and they map the column space to an isomorphic space, so both ranks are preserved. Reducing a matrix to row echelon form through Gaussian elimination therefore leaves the rank unchanged, and in echelon form the rank is simply the number of nonzero rows, which equals the number of pivots.

## Computing rank

The most common method is Gaussian elimination: reduce the matrix to row echelon form and count pivots. For example, the matrix
$$\begin{pmatrix}1&2&1\\-2&-3&1\\3&5&0\end{pmatrix}$$
reduces to
$$\begin{pmatrix}1&0&-5\\0&1&3\\0&0&0\end{pmatrix},$$
which has two nonzero rows, so its rank is 2.

On floating-point computers, basic Gaussian elimination is numerically unreliable because rounding can turn a tiny pivot into zero. Rank-revealing decompositions are safer: the singular value decomposition (SVD) counts nonzero singular values, and QR decomposition with pivoting offers a cheaper alternative. Choosing the threshold that decides when a singular value counts as zero depends on the matrix and the application.

## Equivalent definitions

Rank has several equivalent characterisations, each useful in different contexts:

- The dimension of the image of the linear map $f(x) = Ax$, where $A$ is an $m \times n$ matrix and $f: \mathbb{F}^n \to \mathbb{F}^m$.
- $n$ minus the dimension of the kernel of $f$, by the rank–nullity theorem.
- The number of nonzero singular values in the SVD $A = U\Sigma V^*$.
- The largest order of a nonzero minor of $A$ (determinantal rank).
- The smallest $k$ such that $A$ factors as $A = CR$ with $C$ of size $m \times k$ and $R$ of size $k \times n$ (rank factorisation).
- The smallest $k$ such that $A$ is a sum of $k$ rank-1 matrices (tensor rank), where a rank-1 matrix is an outer product $uv^\mathsf{T}$ of a column and a row.
- For a linear map between any two vector spaces, the dimension of its image.

## Properties

For an $m \times n$ matrix $A$:

- $\operatorname{rank}(A) \le \min(m, n)$. Equality means full rank; a strict inequality means rank-deficient. Only the zero matrix has rank zero.
- $\operatorname{rank}(A) = \operatorname{rank}(A^\mathsf{T})$. A square matrix is invertible if and only if it has full rank.
- For the linear map $f(x) = Ax$: $f$ is injective when $A$ has full column rank (rank $n$), surjective when $A$ has full row rank (rank $m$).
- $\operatorname{rank}(AB) \le \min(\operatorname{rank}(A), \operatorname{rank}(B))$. Multiplying by a full-rank matrix leaves rank unchanged.
- $\operatorname{rank}(A + B) \le \operatorname{rank}(A) + \operatorname{rank}(B)$, and $|\operatorname{rank}(A) - \operatorname{rank}(B)| \le \operatorname{rank}(A + B)$. A consequence is that any rank-$k$ matrix decomposes as a sum of at least $k$ rank-1 matrices.
- For real matrices, $\operatorname{rank}(A^\mathsf{T}A) = \operatorname{rank}(AA^\mathsf{T}) = \operatorname{rank}(A)$. The same chain holds over the complex numbers with the conjugate transpose $A^*$.

Two sharper bounds: Sylvester's rank inequality gives $\operatorname{rank}(A) + \operatorname{rank}(B) - n \le \operatorname{rank}(AB)$ for an $m \times n$ matrix $A$ and an $n \times k$ matrix $B$, and Frobenius's inequality gives $\operatorname{rank}(AB) + \operatorname{rank}(BC) \le \operatorname{rank}(B) + \operatorname{rank}(ABC)$ whenever the products are defined.

## Applications

The Rouché–Capelli theorem links rank to solving $Ax = b$. Comparing the rank of the coefficient matrix $A$ with the rank of the augmented matrix $[A \mid b]$ determines solvability: a larger augmented rank means no solution, equal ranks mean at least one solution, and the solution is unique when the rank equals the number of variables. Otherwise there are $k$ free parameters, where $k$ is the number of variables minus the rank, giving infinitely many solutions over the reals or complexes. Rank also determines controllability and observability in linear control systems, and the rank of a communication matrix bounds the communication required to compute a function in communication complexity.

## Generalisations

Over arbitrary rings the different definitions of rank can diverge or fail to exist. For tensors of order greater than two, tensor rank generalises the idea but is far harder to compute than matrix rank. A smooth map between manifolds has a rank equal to the linear rank of its derivative.

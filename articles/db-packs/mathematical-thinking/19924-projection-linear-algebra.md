# Projection (linear algebra)

A projection is a linear map $P : V \to V$ from a vector space to itself that satisfies $P^2 = P$. Apply it once and the result is fixed: applying $P$ again changes nothing. This idempotence is the defining feature and the source of every property below.

## Image and kernel

Every projection splits $V$ into two complementary subspaces: its image $U = \{Px : x \in V\}$, the subspace it projects onto, and its kernel $\ker P$, the subspace along which it projects. The direct sum $V = U \oplus \ker P$ holds, and $P$ acts as the identity on $U$ while sending every vector in $\ker P$ to zero. For any $x$, the decomposition $x = Px + (x - Px)$ places $Px$ in $U$ and $(I-P)x$ in $\ker P$. The complementary projection $Q = I - P$ projects along $U$ onto $\ker P$. The image and kernel determine a projection's effect, but they do not determine the projection itself: given a fixed image (or kernel), many projections share it, differing in how vectors outside that subspace are mapped in.

A concrete example is $(x,y,z) \mapsto (x,y,0)$ in $\mathbb{R}^3$, which drops the third coordinate onto the $xy$-plane. Its matrix is
$$P = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 0 \end{bmatrix},$$
and $P^2 = P$ together with $P^T = P$ confirms it is idempotent and symmetric.

## Orthogonal and oblique projections

When $V$ carries an inner product, an orthogonal projection is one whose image and kernel are orthogonal subspaces, equivalently $\langle Px, y \rangle = \langle x, Py \rangle$ for all $x, y$. This makes $P$ self-adjoint ($P = P^*$). Any other projection on an inner-product space is oblique. The matrix $P = \begin{bmatrix} 0 & 0 \\ \alpha & 1 \end{bmatrix}$ is a projection for every $\alpha$ because $P^2 = P$, but it is orthogonal only at $\alpha = 0$, where $P^T = P$.

## Eigenvalues and diagonalizability

A projection has only the eigenvalues $0$ and $1$. Its minimal polynomial divides $x^2 - x = x(x-1)$, which splits into distinct factors, so every projection is diagonalizable. In a suitable basis, $P = I_r \oplus 0_{d-r}$, where $r$ is the rank. Orthogonal projections are positive semi-definite, since their eigenvalues are $0$ or $1$.

## Constructing projections

Let $A$ be the $n \times k$ matrix whose columns form an orthonormal basis for a subspace $U$. The orthogonal projection onto $U$ is
$$P_A = A A^T.$$
Without orthonormality, the formula becomes
$$P_A = A (A^T A)^{-1} A^T,$$
which reduces to $AA^T$ when $A^T A = I$. The general oblique projection uses two matrices: $A$ whose columns span the image, and $B$ whose columns span any complement of the kernel, producing
$$P = A (B^T A)^{-1} B^T.$$
Setting $A = B$ recovers the orthogonal case.

## Products and boundedness

The product of two projections need not be a projection. It is a projection exactly when the two projections commute, and commuting orthogonal projections yield an orthogonal projection. On a Hilbert space every orthogonal projection is bounded, with $\|Pv\| \le \|v\|$, because the Cauchy–Schwarz inequality gives $\langle Pv, v \rangle \le \|Pv\| \cdot \|v\|$.

## Continuous projections on normed spaces

In infinite-dimensional normed spaces, a linear projection can fail to be continuous; continuity requires the range to be a closed subspace. In Hilbert spaces, every closed subspace has an orthogonal closed complement, so orthogonal projections are continuous. In a general Banach space, a one-dimensional subspace always admits a closed complement by the Hahn–Banach theorem, but higher-dimensional closed subspaces need not.

# Numerical linear algebra

Numerical linear algebra is the study of how matrix operations become computer algorithms that solve continuous mathematics problems efficiently and accurately. It is a subfield of numerical analysis, and Trefethen and Bau judge it "as fundamental to the mathematical sciences as calculus and differential equations," even though it is comparatively small.

Because computers use floating-point arithmetic and cannot represent irrational numbers exactly, every algorithm applied to real data risks amplifying the gap between a stored value and the true value. Numerical linear algebra uses the structure of vectors and matrices to control that error while keeping computation cheap. Applications mirror those of continuous mathematics itself: signal and image processing, computational finance, fluid dynamics, structural biology, and computational statistics, with matrix methods central to finite difference, finite element, and differential equation models.

## Factor and solve

Most problems reduce to solving $Ax = b$, locating eigenvalues, or fitting data by least squares. The recurring trick is to factor $A$ into simpler matrices, solve the easy pieces, and recombine.

| Factorization | Form | Typical use |
| --- | --- | --- |
| SVD | $A = U\Sigma V^*$, with $U,V$ unitary and $\Sigma$ diagonal (singular values on the diagonal) | Stable least squares, rank, conditioning |
| QR | $A = QR$, $Q$ orthogonal, $R$ upper triangular | Least squares; eigenvalues via the iterative QR algorithm |
| LU | $A = LU$, $L$ lower triangular, $U$ upper triangular | General linear systems |
| Eigendecomposition | $A = X\Lambda X^{-1}$, columns of $X$ are eigenvectors, $\Lambda$ holds eigenvalues | Eigenvalue problems and diagonalising maps |

Gaussian elimination produces an LU factorization by left-multiplying $A$ by successive matrices until it becomes upper triangular. Naive elimination is famously unstable on matrices with many significant digits; pivoting fixes it.

Because singular values are the square roots of the eigenvalues of $AA^*$, most SVD algorithms mirror eigenvalue methods, and Householder procedures are the most common route to both. For least squares, the reduced QR factorization turns $r = b - Ax$ into an upper triangular system $\hat{R}x = \hat{Q}^*b$, and the reduced SVD reduces it to a diagonal system. These paths give QR, Gram–Schmidt, and Householder methods a place alongside the older normal equations.

Numerical linear algebra also shifts how $x = A^{-1}b$ is read: instead of treating $x$ as the product of $A^{-1}$ and $b$, it treats $x$ as the vector of coefficients in the linear expansion of $b$ in the basis formed by the columns of $A$. The column-partition perspective matches the nested loops of matrix code.

## Conditioning and stability

A problem $f:X \to Y$ is ill-conditioned when a small input perturbation $\delta x$ produces a large change $\delta f$ in the output. The condition number
$$\hat{\kappa} = \lim_{\delta\to 0}\sup_{\|\delta x\|\le\delta}\frac{\|\delta f\|}{\|\delta x\|}$$
quantifies this; larger means less well-conditioned. Instability is the tendency of a floating-point algorithm to drift far from the true answer. Householder triangularization stays stable and is a robust choice for linear systems, while the classical normal equations method for least squares is unstable enough that QR and SVD are preferred. Unstable Gram–Schmidt can be rewritten as modified Gram–Schmidt to recover stability, the same role pivoting plays for Gaussian elimination.

## Iterative methods

Two pressures push the field toward iteration. First, no direct method exists for the eigenvalues of an arbitrary matrix, since no program can locate the exact roots of an arbitrary polynomial in finite time, so any general eigensolver must be iterative. Second, a direct algorithm on an $m \times m$ matrix costs $O(m^3)$ time, a high floor given only $m^2$ entries. Iterative methods exploit extra structure, especially sparsity, to skip redundant work.

The workhorse of modern iteration is projection onto a Krylov subspace, building approximations in successively higher dimensions. The conjugate gradient method handles symmetric $Ax = b$; for nonsymmetric systems the generalized minimal residual method and CGN are standard. For eigenvalue problems the Lanczos algorithm applies when $A$ is symmetric, Arnoldi iteration when it is not.

## Origins and software

The field was shaped by John von Neumann, Alan Turing, James H. Wilkinson, Alston Scott Householder, George Forsythe, and Heinz Rutishauser, applying the first machines to ballistics and partial differential equations. The first serious attempt to control computer error was von Neumann and Herman Goldstine's 1947 paper "Numerical inverting of matrices of high order," and growth since has tracked hardware: bigger matrices, higher precision, and parallel computing.

Dedicated environments include MATLAB, Maple, and Mathematica, while general-purpose languages rely on libraries such as LAPACK (used by R), NumPy for Python, and BLAS for C and Fortran.

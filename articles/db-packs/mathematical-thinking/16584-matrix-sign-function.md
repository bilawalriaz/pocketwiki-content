# Matrix sign function

The matrix sign function extends the complex signum function to square matrices. For a complex number, csgn(z) returns 1 when Re(z) > 0 and −1 when Re(z) < 0, ignoring the imaginary part. The matrix analogue csgn(A) plays the same role for a square matrix A, partitioning its dynamics into two halves based on the real parts of its eigenvalues.

The function is well defined for any matrix with no eigenvalue on the imaginary axis, even though the scalar sign function is not analytic. Eigenvalues on the imaginary axis have Re = 0, so the signum rule would be ambiguous there.

## Definition via Jordan form

If A admits the Jordan decomposition

A = P [ J₊  0 ; 0  J₋ ] P⁻¹,

where J₊ contains the Jordan blocks for eigenvalues with positive real part and J₋ those with negative real part, then

csgn(A) = P [ I₊  0 ; 0  −I₋ ] P⁻¹.

A Jordan block is a near-diagonal block whose diagonal entries are the same eigenvalue and whose superdiagonal entries are 0 or 1, encoding the eigenvalue's algebraic and geometric multiplicity. The matrix sign function keeps the same eigenvectors but flips every eigenvalue of negative real part to +1 and every eigenvalue of positive real part to −1, scaled by identity blocks of matching size.

## Core properties

1. csgn(A)² = I, so it is its own inverse.
2. csgn(A) is diagonalizable with eigenvalues only ±1.
3. (I + csgn(A))/2 is a projector onto the invariant subspace for eigenvalues with positive real part (the "right-half plane"), and (I − csgn(A))/2 projects onto the negative real part part ("left-half plane"). A projector is a matrix P satisfying P² = P; here it picks out one half of the spectrum.
4. The Jordan-form formula above.

The combination makes csgn a spectral bisector: it separates the stable and unstable parts of a linear system.

## Computational methods

**Newton iteration.** From the scalar identity csgn(x) = √(x²)/x, one writes csgn(A) = A⁻¹√(A²). Applying the Babylonian averaging method to A² yields

Z_{k+1} = ½ (Z_k + Z_k⁻¹),   Z₀ = A.

Convergence is global and locally quadratic.

**Newton–Schulz iteration.** Inverting Z_k at every step is expensive. Replacing Z_k⁻¹ with Schulz's 1933 one-step approximation Z_k(2I − Z_k²) gives

Z_{k+1} = ½ Z_k (3I − Z_k²).

This needs only matrix products, no inversions. Convergence stays quadratic but is only local, guaranteed when ‖I − A²‖ < 1.

## Applications

**Sylvester equations.** For stable A and B, the unique solution X of AX + XB = C is recovered as

[ −I  2X ; 0  I ] = csgn ( [ A  −C ; 0  −B ] ).

The Lyapunov equation AX + XAᵀ = C is a special case, and there the Newton iteration simplifies to use only inverses of A and Aᵀ.

**Algebraic Riccati equations.** For AᴴP + PA − PFP + Q = 0, under Hermitian F, Q and the existence of a unique stabilizing solution, set

[ V  W ] = csgn ( [ Aᴴ  Q ; F  −A ] ) − [ I  0 ; 0  I ].

Then P = −V⁻¹W solves the equation.

**Matrix square root.** The Denman–Beavers iteration for √A falls out of the Newton method for csgn by observing that A − PIP = 0 is a degenerate algebraic Riccati equation, whose solution P is, by construction, √A.

Source: adapted from "Matrix sign function" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Matrix_sign_function

# Calculus of moving surfaces

The calculus of moving surfaces (CMS) is an extension of classical tensor calculus to deforming manifolds—surfaces whose shape changes with time, like a flag in the wind. Its central object is the tensorial time derivative ∇̇, originally defined by Jacques Hadamard, which plays the same role for time evolution that the covariant derivative ∇_α plays for spatial differentiation on differential manifolds: when applied to a tensor, ∇̇ returns a tensor.

## Surface velocity C

Let Σ_t be the position of a surface Σ at time t. The surface velocity C measures how fast Σ moves in its instantaneous normal direction at a point P:

C = lim_{h→0} Distance(P, P*) / h

where P* is the point on the surface at time t+h lying along the line perpendicular to Σ_t at P. C is signed: positive when the displacement points along the chosen normal, negative when it points opposite. The pair (Σ_t, C) mirrors position and velocity in elementary calculus—each determines the other by integration or differentiation.

## The tensorial time derivative ∇̇

For a scalar field F defined on Σ_t, the geometric definition of ∇̇ is the rate of change of F in the instantaneously normal direction:

δF/δt = lim_{h→0} [F(P*) − F(P)] / h

These geometric limits can be awkward to apply directly, so the CMS also gives analytical formulas in the standard operations of calculus and differential geometry.

## Analytical definitions

Parametrise the evolving surface as Z^i = Z^i(t, S), where Z^i are general curvilinear space coordinates and S^α are surface coordinates (indices on arguments dropped by convention). Define the velocity object V = V^i Z_i with V^i = ∂Z^i(t, S)/∂t. The surface velocity is then C = V^i N_i, where N_i are the covariant components of the normal vector N⃗.

Introduce the shift tensor Z^α_i = S^α · Z_i relating the surface tangent space to the ambient basis, and the tangent velocity V^α = Z^α_i V^i. For an invariant scalar field F:

∇̇ F = ∂F(t, S)/∂t − V^α ∇_α F

where ∇_α is the covariant derivative on Σ. For a representative tensor T^{iα}_{jβ}:

∇̇ T^{iα}_{jβ} = ∂T^{iα}_{jβ}/∂t − V^η ∇_η T^{iα}_{jβ} + V^m Γ^i_{mk} T^{kα}_{jβ} − V^m Γ^k_{mj} T^{iα}_{kβ} + Γ̇^α_η T^{iη}_{jβ} − Γ̇^η_β T^{iα}_{jη}

Here Γ^m_{jk} are Christoffel symbols and Γ̇^α_β = ∇_β V^α − C B^α_β are the surface's temporal Christoffel symbols, with B^α_β the matrix representation of the shape operator.

## Properties of ∇̇

∇̇ commutes with index contraction and satisfies the product rule ∇̇(S^i_α T^β_j) = T^β_j ∇̇ S^i_α + S^i_α ∇̇ T^β_j. For surface restrictions of spatial tensors it obeys a chain rule:

∇̇ F^j_k(Z, t) = ∂F^j_k/∂t + C N^i ∇_i F^j_k

As a consequence, the ∇̇-derivatives of all spatial metric structures vanish: ∇̇ δ^i_j = 0, ∇̇ Z_{ij} = 0, ∇̇ Z^{ij} = 0, ∇̇ ε_{ijk} = 0, ∇̇ ε^{ijk} = 0. In general coordinates the Levi-Civita symbols carry a factor of √|det Z_{ij}|, and the rule still holds.

## Differentiation table for surface objects

Applied to the fundamental surface objects, ∇̇ produces compact identities. The surface metric tensors are annihilated:

∇̇ S_{αβ} = 0,  ∇̇ S^{αβ} = 0

For the curvature tensors B_{αβ}, B^α_β, and B^{αβ}:

∇̇ B_{αβ} = ∇_α ∇_β C + C B_{αγ} B^γ_β
∇̇ B^α_β = ∇_β ∇^α C + C B^α_γ B^γ_β
∇̇ B^{αβ} = ∇^α ∇^β C + C B^{γα} B_γ^β

The shift tensor and normal couple through the gradient of C:

∇̇ Z^α_i = N^i ∇_α C,  ∇̇ N^i = −Z^α_i ∇^α C

The surface Levi-Civita symbols satisfy ∇̇ ε_{αβ} = 0 and ∇̇ ε^{αβ} = 0. These identities, together with the chain rule, govern the time differentiation of volume and surface integrals over a deforming surface.

Source: adapted from "Calculus of moving surfaces" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Calculus_of_moving_surfaces

# Electric potential energy

Electric potential energy is the energy a charge possesses by virtue of its position within an electric field created by other charges. It is measured in joules (SI) and, in atomic-scale contexts, electronvolts (1 eV = 1.602×10⁻¹⁹ J).

A central distinction separates two regimes. Electrostatic potential energy applies to time-invariant fields, where Coulomb forces are conservative and energy depends only on configuration. The broader term electric potential energy covers systems with time-variant electric fields, where the configuration-only definition no longer suffices.

## How it is defined

The electrostatic potential energy of a charge *q* is the work an external agent must do to bring *q* from a reference position (usually infinity) to its final location *r*, without acceleration. Equivalently, it is the negative of the work done by the electrostatic force during that assembly.

In a static field **E**, this gives the path-independent line integral

U_E(**r**) = −∫_{**r**_ref}^{**r**} q **E**(**r**′) · d**r**′

Because the field is conservative, only the endpoints matter. Using the electric potential *V* (the potential created by all other charges at position **r**), the definition collapses to

U_E = qV(**r**)

This identity, U = qV, is the operational bridge between field-based and potential-based thinking.

## Two point charges

For a point charge *q* at distance *r* from another point charge *Q*, with infinite separation as reference, Coulomb's law integrates to

U_E = (1/4πε₀)(qQ/r) = k_e qQ/r

The signs of the charges are preserved, so opposite charges yield negative energy and like charges yield positive energy. A single isolated charge has zero electrostatic potential energy: there is no other source of field against which work must be done. A charge does not interact with its own field, so self-energy contributes nothing to the stored value.

## Multiple charges

For one charge *q* in the presence of *n* fixed charges *Q_i* at distances *r_i*,

U_E = (q / 4πε₀) Σ Q_i / r_i

The stored energy of a system of *N* charges requires a factor of one-half to avoid double-counting each pair:

U_E = ½ Σ_i q_i V(**r**_i) = ½ k_e Σ_i Σ_{j≠i} q_i q_j / r_ij

For three charges, this expands explicitly to

U_E = (1/4πε₀) [ Q₁Q₂/r₁₂ + Q₁Q₃/r₁₃ + Q₂Q₃/r₂₃ ]

The double sum makes the physical meaning clear: energy is stored in every pairwise interaction, and the half corrects for counting each pair twice.

## Energy density of a field

The total energy can be written as a volume integral over the field rather than over the charges. In vacuum the energy density at each point is

u_e = ½ ε₀ |**E**|²

A capacitor stores this kind of field energy. For a capacitor of capacitance *C* charged to potential difference *V* with charge *Q*,

U_E = ½ QV = ½ CV² = Q²/(2C)

This follows by summing the infinitesimal work dW = V dq required to add each charge increment. The same form generalises to dielectrics via the displacement field **D**: U_E = ½ ∫ **E** · **D** dV, with the integral over the dielectric volume.

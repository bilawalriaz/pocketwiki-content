# Bi-isotropic material

A bi-isotropic material is an isotropic medium in which the electric and magnetic fields are coupled, so an electric field can produce a magnetic response and a magnetic field can produce an electric response. A major subset, called Pasteur media, rotates the polarisation of light because of this coupling. The rotation arises from the chirality or non-reciprocity of the medium's structure, not simply from a twisting effect. The acoustic analogue of this electric-magnetic coupling is called Willis coupling.

## Constitutive relations

In ordinary isotropic media the electric field E and electric displacement D are parallel, and the magnetic field H and magnetic flux density B are also parallel, with constants of proportionality ε (permittivity) and μ (permeability). In bi-isotropic media the two pairs are linked by two extra scalar coupling terms:

D = εE + ξH
B = μH + ζE

Here ε and μ are the usual permittivity and permeability, while ξ and ζ are the magnetoelectric coupling constants, intrinsic to each medium. If these four quantities are direction-dependent tensors rather than scalars, the medium is called bi-anisotropic.

## Tellegen and chirality parameters

The two coupling constants can be rewritten using the Tellegen (reciprocity) parameter χ and the chirality parameter κ:

χ − iκ = ξ / √(εμ)
χ + iκ = ζ / √(εμ)

Substituting back gives:

D = εE + (χ − iκ)√(εμ) H
B = μH + (χ + iκ)√(εμ) E

The frequency dependence of κ can be modelled with the Condon model.

## Classification

| | Reciprocal (χ = 0) | Non-reciprocal (χ ≠ 0) |
|---|---|---|
| **Non-chiral (κ = 0)** | Simple isotropic medium | Tellegen medium |
| **Chiral (κ ≠ 0)** | Pasteur medium | General bi-isotropic medium |

A Pasteur medium is reciprocal and chiral, so ξ = −ζ and the only coupling is a handedness-driven cross term. A Tellegen medium is non-reciprocal and non-chiral, so ξ = ζ and the cross term is symmetric. The general case combines both.

## Examples

Pasteur media can be made by embedding tiny metal helices of one handedness into a resin. The helices must be randomly oriented to keep the overall medium isotropic. Geometrically a helix behaves like an inductor: the magnetic component of an incident wave drives a current along the wire, which then re-radiates and modifies the electric component. With χ = 0 the constitutive relation reduces to D = εE − iκ√(εμ) H, meaning the D response carries a 90° phase delay relative to the H drive.

Tellegen media work the other way around, through an electromagnetic link rather than geometry. A typical realisation bonds electric dipoles to small magnets. When the dipoles line up with the electric field of an incident wave, the attached magnets rotate with them, perturbing the magnetic component of the wave. With κ = 0 the relation becomes B = μH + χ√(εμ) E, so the B response stays in phase with H. Because the coupling is electromagnetic rather than geometric, Tellegen media have no simple handedness.

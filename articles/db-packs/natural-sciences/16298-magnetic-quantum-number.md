# Magnetic quantum number

The magnetic quantum number specifies the orientation of an electron's angular momentum in space. For each type of angular momentum in an atom there is a matching magnetic quantum number, and its allowed values are restricted to a fixed integer range set by the related angular-momentum quantum number. The "magnetic" label reflects the fact that states with different magnetic quantum numbers shift in energy when a magnetic field is applied, a behaviour known as the Zeeman effect.

## The four quantum numbers for an atomic electron

A single electron in an atom is described by four quantum numbers:

- Principal quantum number *n* (size and energy of the orbital)
- Azimuthal quantum number *ℓ* (shape: 0 for s, 1 for p, 2 for d, 3 for f)
- Orbital magnetic quantum number *mℓ* (orientation of the orbital)
- Spin magnetic quantum number *mₛ* (orientation of spin)

Spin is an intrinsic angular momentum. For an electron *s* = ½, so *mₛ* takes exactly two values, +½ and −½, conventionally labelled "spin-up" and "spin-down" (α and β). Orbital angular momentum comes from the electron's motion around the nucleus and is described by *ℓ* and *mℓ*.

## Orbital magnetic quantum number *mℓ*

For a given *ℓ*, the allowed values of *mℓ* run as the integers:

*mℓ* = −*ℓ*, −*ℓ*+1, …, 0, …, +*ℓ*−1, +*ℓ*

There are 2*ℓ*+1 of them. The corresponding orbital has a definite component of angular momentum along a chosen axis, conventionally *z*:

*Lz* = *mℓ* ℏ

ℏ is the reduced Planck constant. The magnitude of the total orbital angular momentum is *L* = ℏ√(*ℓ*(*ℓ*+1)), which is always larger than *Lz* except when *ℓ* = 0, so the angular momentum vector cannot be aligned with the *z*-axis. It is also impossible to measure *L* along all three axes at once; this constraint was first demonstrated in the Stern–Gerlach experiment.

Each orbital can hold two electrons with opposite spins, and the number of orbitals per subshell grows with *ℓ*:

| Subshell | *ℓ* | Orbitals | Electrons |
|----------|-----|----------|-----------|
| s | 0 | 1 | 2 |
| p | 1 | 3 | 6 |
| d | 2 | 5 | 10 |
| f | 3 | 7 | 14 |
| g | 4 | 9 | 18 |

This count underlies the structure of the periodic table.

## Where *mℓ* comes from

For a hydrogen-like atom the Schrödinger equation separates in spherical coordinates into a radial part *R(r)*, a polar-angle part *P(θ)*, and an azimuthal part *F(φ)*:

ψ(r, θ, φ) = R(r) · P(θ) · F(φ)

The azimuthal equation has solutions *F(φ)* = *A* *e*^(λφ). Because φ and φ + 2π describe the same point in space, the magnitude of *F* cannot grow with φ, which forces λ to be a pure imaginary number λ = *i mℓ*. The integer *mℓ* that emerges is the orbital magnetic quantum number. The same constant appears in the polar-angle equation: larger |*mℓ*|² reduces the magnitude of *P(θ)*, and |*mℓ*| greater than *ℓ* admits no solution at all.

## Behaviour in magnetic fields

In the absence of a magnetic field, all orbitals with the same *n* and *ℓ* have the same energy regardless of *mℓ*; their spherical harmonics differ only in orientation. An external magnetic field breaks this symmetry through the Zeeman effect, splitting each subshell into 2*ℓ*+1 levels with distinct energies. Both the orbital and spin magnetic moments contribute to the splitting, and the torque on the magnetic moment produces Larmor precession about the field direction.

## Other magnetic quantum numbers

The same idea generalises to other angular momenta: *mj* labels the *z*-component of the total electronic angular momentum *j*, and *mI* labels the *z*-component of nuclear spin *I*. Capital letters (*ML*, *MS*, …) denote totals for a system of particles rather than a single one.

Source: adapted from "Magnetic quantum number" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Magnetic_quantum_number

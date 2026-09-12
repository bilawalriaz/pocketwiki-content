# Refractive index and extinction coefficient of thin film materials

Two quantities, the refractive index *n* and the extinction coefficient *k*, describe how a material interacts with light: *n* governs refraction (how light slows and bends at an interface) and *k* governs absorption (how strongly light intensity drops inside the material). Both depend on photon energy *E*, so they are written *n(E)* and *k(E)*. They are often called the "optical constants" of a material, though they are not truly constant. Since *E = hc/λ*, where *h* is Planck's constant and *c* the speed of light in vacuum, the spectra can equivalently be expressed as *n(λ)* and *k(λ)*.

## The Forouhi–Bloomer dispersion equations

A. R. Forouhi and I. Bloomer derived dispersion equations for *n(E)* and *k(E)*, published in 1986 for amorphous materials and in 1988 for crystalline materials, and later included in *The Handbook of Optical Constants* (1991). The derivation starts from first-principles quantum mechanics and solid-state physics: an expression for *k(E)* is obtained from the underlying electronic transitions, and *n(E)* is then recovered from *k(E)* via the Kramers–Kronig relations. Kramers–Kronig enforces causality (no response before a stimulus) and states that *n(E)* is the Hilbert transform of *k(E)*, a linear integral transform that pairs the real and imaginary parts of any causal response function.

For amorphous materials:

*k(E) = A(E − E_g)² / (E² − BE + C)*

*n(E) = n(∞) + (B₀E + C₀) / (E² − BE + C)*

Five independent parameters fix both spectra:

| Parameter | Meaning |
|---|---|
| *E_g* | Optical energy band gap of the material |
| *A, B, C* | Set by the band structure; positive constants with 4*C* − *B*² > 0 |
| *n(∞)* | Value of *n* as *E* → ∞, greater than 1 |
| *B₀, C₀* | Not independent; derived from *A, B, C, E_g* |

For crystalline materials, whose spectra show multiple peaks, each equation becomes a sum of *q* terms, one per peak:

*k(E) = Σᵢ [ Aᵢ(E − E_g,i)² / (E² − BᵢE + Cᵢ) ]*

*n(E) = n(∞) + Σᵢ [ (B₀,ᵢE + C₀,ᵢ) / (E² − BᵢE + Cᵢ) ]*

Every term carries its own *Aᵢ, Bᵢ, Cᵢ, E_g,i* and derived *B₀,ᵢ, C₀,ᵢ*, with the same physical meaning as in the amorphous case.

## Scope and alternatives

The equations were intended for semiconductors and dielectrics in amorphous, polycrystalline, or crystalline forms, but also describe transparent conductors such as indium tin oxide (ITO), metallic compounds, and polymers. Polymers are treated as "crystalline" here because photoresists and similar long-chain materials, though they lack a classical crystal lattice, show multiple sharp peaks in *n* and *k* rather than the single broad maximum typical of amorphous films.

Other dispersion models exist. The Tauc–Lorentz model handles absorbing materials in another parameterisation. Cauchy and Sellmeier give empirical expressions for *n* over a limited wavelength range and only apply where *k* = 0, so they fail for absorbing films.

## Characterizing thin films

Thin-film coatings on substrates are essential to microfabrication, and their *n*, *k*, and thickness *t* must be measured and controlled for repeatable manufacturing. The *n* and *k* spectra cannot be measured directly; they are inferred from quantities that depend on them, principally spectroscopic reflectance *R(λ)* and, for transparent substrates, spectroscopic transmittance *T(λ)*. The procedure combines the Forouhi–Bloomer equations for *n(λ)* and *k(λ)* with the Fresnel equations for reflection and transmission at an interface, producing theoretical expressions for *R* and *T*. A nonlinear least-squares regression then iteratively adjusts *A, B, C, E_g, n(∞)* and *t* to minimise the error between the theoretical and measured spectra. Spectroscopic ellipsometry works on the same principle.

## Practical complications

Multi-film stacks make regression harder, because the theoretical reflectance must include *n*, *k*, and *t* for every layer, and a non-linear fit may not converge to a unique solution. Two strategies help. First, fix *n* and *k* of known layers (such as an SiO₂ film on a silicon wafer) and vary only the unknowns; this resolved a 1147 nm amorphous silicon film on SiO₂/Si. Second, when parameters remain ambiguous, deposit the same film on two different substrates and fit both data sets simultaneously, a multi-spectral analysis. For a Ge₄₀Se₆₀ film this gave 34.5 nm on silicon and 33.6 nm on oxidised silicon, with a 166 nm oxide thickness, all from one consistent pair of *n* and *k* spectra.

Periodic trench structures, which repeat with a given pitch, are characterised by combining Forouhi–Bloomer-derived *n* and *k* of each material with Rigorous Coupled-Wave Analysis (RCWA), a numerical method for solving Maxwell's equations in periodic geometries. Measuring polarised broadband reflectance *Rs* and *Rp* over 190–1000 nm yields trench depth, critical dimensions at top, middle, and bottom, and sidewall angle. A trench with 160 nm pitch was profiled down to features of order tens of nanometres (for example, Si depth 27.4 nm, Poly-Si width 92.6 nm), using fixed tables for known films and a separately measured blanket film for the unknown one.

For polymers such as 248 nm photoresist, most spectral structure lies in the deep UV, so accurate reflectance below ~300 nm is essential; a 498 nm photoresist on silicon required six terms in the crystalline sum. For transparent conductors like ITO, *k(λ)* ≈ 0 in the visible, rises to about 0.05 in the near-infrared, and peaks further into the infrared, where the material behaves like a metal. A 133 nm ITO film on glass was characterised by fitting *R* and *T* together, after first using the bare substrate's spectra to extract the previously unknown *n* and *k* of the glass.

The standard measurement window of 190–1000 nm covers the spectral features that distinguish amorphous, polycrystalline, and crystalline behaviour, and includes most of the absorbing structure of polymers and transparent conductors.

Source: adapted from "Refractive index and extinction coefficient of thin film materials" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Refractive_index_and_extinction_coefficient_of_thin_film_materials

# Liquid

## Overview
A liquid is a state of matter characterized by a definite volume but no fixed shape, adapting to its container while remaining nearly incompressible. It consists of atoms or molecules held by intermediate-strength intermolecular forces, allowing particles to move past one another while staying densely packed—distinct from rigid solids and diffuse gases. Liquids are a form of condensed matter alongside solids and a form of fluid alongside gases. They exist only within a narrow temperature and pressure range, making them the least common state of matter in the known universe despite water's abundance on Earth. Understanding liquids requires bridging microscopic structure (short-range order, energy-entropy competition) with macroscopic properties (viscosity, surface tension, hydraulics) and phase behavior.

## Timeline
- **Ancient times** — Pumps and waterwheels used to convert liquid motion into mechanical work.
- **Classical antiquity** — Archimedes formulates principle of buoyancy (force equals weight of displaced fluid).
- **17th century** — Pascal's law established: pressure change in confined incompressible fluid transmits undiminished.
- **19th century** — Navier-Stokes equations developed describing viscous fluid flow.
- **20th century** — X-ray/neutron diffraction reveals absence of long-range order; static structure factor *S(q)* and radial distribution function *g(r)* characterize short-range order.
- **Mid-20th century** — Molecular dynamics (MD) simulations begin using Newton's laws to model liquid trajectories.
- **Late 20th century** — Ab initio quantum molecular dynamics developed; lattice Boltzmann and other mesoscopic methods emerge.
- **Contemporary** — Liquid metals (e.g., gallium) proposed for soft robotics and wearable devices due to conductivity and deformability.

## Body

### Definition and Classification
A liquid possesses a definite volume but no fixed shape, conforming to its container under forces like gravity. It is nearly incompressible, with density close to solids and far higher than gases. Liquids are classified as **condensed matter** (with solids) due to high density, and as **fluids** (with gases) due to ability to flow. The state arises from intermolecular bonds of intermediate strength: stronger than gases (allowing particle mobility) but weaker than solids (preventing fixed positions). Only mercury and bromine are elemental liquids at standard temperature and pressure; francium, caesium, gallium, and rubidium melt slightly above room temperature.

### Phase Transitions and Thermodynamics
Liquids exist in a narrow temperature/pressure window. Heating increases molecular vibration and separation; at the **boiling point**, cohesive forces fail and the liquid becomes gas. Cooling reduces separation; at the **freezing point**, molecules typically crystallize into a structured solid. Below the boiling point, liquid and vapor reach equilibrium (evaporation = condensation); if vapor is removed, the liquid cannot persist. Below freezing, crystallization proceeds to completion under constant pressure unless **supercooling** occurs. In vacuum (near-zero pressure), liquids cannot exist—they either boil or freeze depending on temperature. Water in space sublimes in sunlight and freezes in shadow; ice persists only in permanently shadowed craters (e.g., Moon) or beyond Saturn's orbit where solar flux is too low for sublimation.

### Microscopic Structure: Short-Range Order and Energy-Entropy Balance
Liquids lack the long-range translational order of crystals but possess **short-range order** persisting over a few molecular diameters. Excluded volume interactions induce positional order (nearest neighbors at ~integer multiples of molecular diameter). In non-spherical molecules (e.g., water), directional forces (hydrogen bonds) create orientational order, forming dynamic, transient networks/clusters. **Liquid crystals** are a distinct state: they flow like liquids but exhibit long-range orientational alignment without translational order.

The structure emerges from competition between attractive intermolecular forces (pulling molecules together) and **entropic forces** (driving them apart to maximize volume/entropy). In gases, entropy dominates; in solids, energy dominates; in liquids, they are comparable—binding energy ~ thermal energy *k*<sub>B</sub>*T*. This balance creates **no small parameter** for perturbation theory: unlike gases (ideal gas reference, density as small parameter) or solids (perfect lattice reference, thermal motion as small parameter), liquids lack a tractable reference state, making theoretical modeling difficult.

### Quantum and Classical Regimes
Liquids are fundamentally quantum mechanical, but often behave classically at macroscopic scales. The **thermal de Broglie wavelength** Λ = (2πℏ²/*mk*<sub>B</sub>*T*)<sup>1/2</sup> must be small compared to intermolecular spacing *a* ≈ *ρ*<sup>−1/3</sup> for classical statistical mechanics to apply. Typical Λ ~ 0.01–0.1 nm; Λ/*a* ≪ 1 holds for most room-temperature liquids. Quantum effects (zero-point motion, tunneling) matter for light molecules (H, He) at low temperatures, and for hydrogen bonding (proton mass). Dynamic processes require timescale *τ* ≫ *h*/*k*<sub>B</sub>*T* (~10<sup>−14</sup> s at room temperature) for classical description.

### Dynamic Phenomena and Relaxation
Sound speed *c* = √(*K*/*ρ*) depends on bulk modulus *K*. All liquids show **dispersion**: *K* crosses from low-frequency liquid-like limit *K*<sub>0</sub> to high-frequency solid-like limit *K*<sub>∞</sub> at GHz–THz frequencies (**hypersound**). Shear modulus *G* is zero at zero frequency (defining property of a liquid) but also crosses over at hypersound. This crossover is a **relaxation**—Fourier transform of *K* or *G* describes return to equilibrium after perturbation. Upon supercooling toward the glass transition, structural relaxation time increases exponentially, causing viscoelastic behavior.

### Experimental Probes
Absence of long-range order means no Bragg peaks in X-ray/neutron diffraction. Patterns show circular symmetry (isotropy) with radial oscillations described by the **static structure factor** *S*(*q*), where *q* = (4π/λ) sin θ. Oscillations in *S*(*q*) reflect neighbor-shell correlations. The **radial distribution function** *g*(*r*) (Fourier transform of *S*(*q*)) gives spatial average of pair correlations in a temporal snapshot.

### Macroscopic Properties

**Volume and Compressibility:** Volume fixed by *T* and *P*; liquids expand on heating (water 0–4 °C contracts). Compressibility is negligible: water compresses 46.4 ppm/bar; 4000 bar yields only 11% volume reduction. This enables **hydraulics** (Pascal's law: pressure change transmits undiminished) but causes **water hammer** (pressure spike from sudden valve closure) and **cavitation** (low-pressure vapor bubbles collapse violently in high-pressure zones, eroding surfaces).

**Pressure and Buoyancy:** In a gravitational field, pressure increases with depth: *p* = *p*<sub>0</sub> + *ρgz*. **Archimedes' principle**: buoyant force = weight of displaced fluid; direction depends on object density relative to liquid.

**Surfaces and Surface Tension:** Surface molecules experience net inward pull due to asymmetric bonding. **Surface tension** (energy/area, J/m²) is a material property; liquids minimize surface area (spherical drops). It governs wettability, capillary action, waves, and ripples. Under nanoscale confinement, surface effects dominate. Common liquids: tens of mJ/m²; liquid metals (mercury): hundreds of mJ/m².

**Flow and Viscosity:** **Viscosity** measures resistance to shear deformation (e.g., pipe flow: slower near walls). It decreases with temperature. **Newtonian liquids** (water, glycerin, motor oil, honey, mercury) have constant viscosity independent of shear rate/history. **Non-Newtonian liquids** (ketchup, custard, starch solutions) thicken or thin under shear. Viscosity control via blending or additives (viscosity index) is critical for lubrication.

**Sound Propagation:** Speed *c* = √(*K*/*ρ*). Example: water *K* ≈ 2.2 GPa, *ρ* = 1000 kg/m³ → *c* ≈ 1.5 km/s.

### Solutions and Mixtures
Liquids form solutions with gases, solids, and other liquids. **Miscible** liquids mix in any proportion (water/ethanol); **immiscible** do not (water/gasoline). **Emulsions** stabilize immiscible mixtures via surfactants (e.g., mayonnaise: water/oil stabilized by lecithin). **Eutectic mixtures** (e.g., NaK alloy) are liquid at room temperature despite solid components. Everyday mixtures: aqueous solutions (bleach), emulsions (vinaigrette), suspensions (blood), colloids (paint, milk). Gases liquefied by cooling: liquid O₂, N₂, H₂, He. CO₂ solidifies directly (dry ice) at 1 atm; liquefies only above 5.1 atm. Liquid helium remains liquid at 0 K under standard pressure due to quantum effects.

### Applications
- **Lubrication:** Thin flowing layers reduce friction; oils chosen for viscosity/temperature stability (engines, gearboxes, hydraulics).
- **Solvation:** Solvents dissolve solids/liquids (paints, adhesives, cleaning agents like naphtha/acetone). Surfactants in soaps/detergents; alcohol as antimicrobial; extraction of vegetable oil.
- **Cooling:** High thermal conductivity + flow removes heat. Water/glycol in engines; water/liquid metals (Na, Bi) in nuclear reactors; liquid propellant films in rockets; cutting fluids in machining; sweat evaporation; HVAC heat transfer.
- **Cooking:** Heat transfer via conduction and convection (low kinematic viscosity → constant-temperature convection). **Steaming** exploits latent heat: phase change at boiling point absorbs/releases energy at constant temperature.
- **Distillation:** Separation by boiling-point differences (alcoholic beverages, oil refineries, cryogenic distillation of Ar, O₂, N₂, Ne, Xe via liquefaction).
- **Hydraulics:** Pascal's law provides fluid power. Pumps/waterwheels (ancient); hydraulic presses (lifting, forming); brakes, transmissions, heavy equipment, aircraft controls.
- **Liquid Metals:** Electrical conductivity + incompressibility + deformability → soft robotics, wearable sensors. Gallium favored: liquid near room temperature, low toxicity, low volatility.
- **Measuring Devices:** Thermometers (thermal expansion of Hg/alcohol); manometers (liquid weight indicates pressure). **Liquid-mirror telescopes**: rotating liquid (Hg) forms paraboloid; cheaper than glass but zenith-only.

### Prediction of Liquid Properties
Methods organized by length/time scale:
- **Macroscopic:** Empirical correlations (e.g., *η*(*T*) = *Ae*<sup>*B*/*T*</sup>) fit experimental data; efficient but cannot extrapolate. **Thermodynamic potentials** (e.g., Gibbs free energy *G*(*p*,*T*)): one function yields all equilibrium properties via derivatives. **Hydrodynamics** (Navier-Stokes): PDEs for density, velocity, temperature fields; generalizes beyond equilibrium.
- **Mesoscopic:** Intermediate scales; combine continuum and particle dynamics. **Lattice Boltzmann**: fictitious particles on lattice stream and collide (coarse-grained Boltzmann equation). Others: smoothed-particle hydrodynamics, dissipative particle dynamics, multiparticle collision dynamics.
- **Microscopic:** **Classical molecular dynamics (MD)**: Newton's laws (*F*=*mẍ*) trace trajectories; requires intermolecular force models (from experiment/fitting). **Ab initio quantum MD**: forces from quantum mechanics/fundamental constants; no experimental input needed but computationally expensive for large molecules.

## Terms
- ****Condensed matter**** — Phases with high density and strong intermolecular interactions (solids and liquids).
- ****Fluid**** — Substance that continuously deforms under shear stress (liquids and gases).
- ****Intermolecular forces**** — Forces between molecules; intermediate strength in liquids allows mobility without dissociation.
- ****Short-range order**** — Structural correlation persisting over a few molecular diameters; positional and/or orientational.
- ****Entropic forces**** — Effective forces driving system toward maximum entropy (volume expansion); not mechanical forces.
- ****Thermal de Broglie wavelength (Λ)**** — Quantum length scale Λ = (2πℏ²/*mk*<sub>B</sub>*T*)<sup>1/2</sup>; classical behavior requires Λ ≪ intermolecular spacing.
- ****Surface tension**** — Energy per unit area (J/m²) to create a surface; arises from asymmetric bonding at interface.
- ****Viscosity**** — Resistance to shear deformation/flow; decreases with temperature; Newtonian (constant) or non-Newtonian (shear-dependent).
- ****Bulk modulus (K)**** — Measure of incompressibility; relates pressure change to fractional volume change; determines sound speed *c* = √(*K*/*ρ*).
- ****Static structure factor S(q)**** — Diffraction intensity vs. wavenumber *q*; oscillations reveal neighbor-shell correlations in liquids.
- ****Radial distribution function g(r)**** — Fourier transform of *S(q)*; spatial average of pair correlations (probability of finding a particle at distance *r*).
- ****Miscible/Immiscible**** — Liquids that form solutions in any proportion vs. those that do not.
- ****Eutectic mixture**** — Mixture with melting point lower than any component; liquid at temperatures where pure components are solid.
- ****Pascal's law**** — Pressure change in confined incompressible fluid transmits undiminished throughout.
- ****Navier-Stokes equations**** — PDEs governing time evolution of density, velocity, temperature in viscous fluids.
- ****Lattice Boltzmann method**** — Mesoscopic simulation: fictitious particles on lattice stream and collide; coarse-grained kinetic theory.
- ****Ab initio molecular dynamics**** — Quantum mechanical simulation where forces are computed from electronic structure, not fitted.

## Debates and open questions
- **No small parameter problem:** The energy-entropy balance in liquids prevents systematic perturbation theory; no universal reference state exists (unlike ideal gas or perfect crystal).
- **Glass transition mechanism:** Exponential growth of structural relaxation time upon supercooling leads to viscoelasticity and glass formation; microscopic theory remains incomplete.
- **Quantum effects in hydrogen bonding:** Proton zero-point motion and tunneling in water and associated liquids require quantum treatment even at room temperature.
- **Ab initio prediction:** Computational cost limits quantum MD to small systems/short times; accurate classical force fields still rely on experimental fitting.
- **Liquid-liquid phase transitions:** Hypothesized transitions between distinct liquid structures (e.g., in water, silicon) remain experimentally and theoretically debated.

Source: adapted from "Liquid" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Liquid

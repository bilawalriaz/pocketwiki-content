# Accelerator physics

Accelerator physics is a branch of applied physics concerned with designing, building, and operating particle accelerators. Its subject is the motion, manipulation, and observation of relativistic charged particle beams and their interaction with accelerator structures through electromagnetic fields. The field draws on microwave engineering (for radio-frequency acceleration and deflection structures), geometrical optics (for beam focusing and bending), laser physics, digital signal processing, and plasma physics, while the experiments performed with the resulting beams belong to particle, nuclear, condensed-matter, or materials physics. The kinds of experiments a given facility can host are set by the beam's average energy, particle type, intensity, and dimensions.

## Why radio-frequency fields, and why a vacuum

Charged particles can in principle be accelerated by a static voltage, as in a Cockcroft-Walton multiplier, but two limits stop this approach at high energy. The electrostatic field breaks down above some voltage, and because it is conservative, the maximum voltage directly caps the kinetic energy a particle can gain.

Particle accelerators therefore use time-varying fields instead. To propagate those fields through hollow structures the particles also pass through, the frequency must sit in the radio-frequency region of the electromagnetic spectrum, where the wavelength is long enough to fit inside the structure. A linear accelerator (linac) is the simplest example of this principle.

Because the beam would otherwise scatter off gas molecules, the space around it is evacuated inside a beam pipe. The strong electromagnetic field that travels with the beam, however, can still interact with the pipe's walls. Any resistive wall or geometric change in cross section presents a resistive, inductive, or capacitive impedance, and the beam excites wakefields in response. These wakefields are distortions of the beam's own field that can act on later particles, so their magnitude is calculated and reduced.

## Beam dynamics: bending, focusing, and the equation of motion

At relativistic speeds the Lorentz force from magnetic fields dominates beam steering, so beam direction is mainly set by magnetostatic fields produced by dedicated electromagnets. The breakthrough that made modern accelerators possible was strong focusing, in which alternating magnetic gradients confine a beam far more tightly than any single uniform field could.

Different magnet types play distinct roles. Dipole magnets guide the beam along the design orbit, quadrupole magnets focus it transversely, and sextupole magnets correct dispersion, the spread of trajectories caused by momentum spread in a bending magnet. A quadrupole's action on a beam is directly analogous to a lens in geometrical optics: it focuses in one transverse plane while defocusing in the other, and the alternating-gradient arrangement of strong focusing turns this apparent weakness into net confinement. Static electric or magnetic fields cannot focus a stationary or slowly moving charged particle, which is why quadrupole arrangements are needed in the first place.

A particle on the exact design orbit feels only dipole field components. A particle displaced by x(s) at path length s obeys, to first order and neglecting higher multipoles, the inhomogeneous Hill equation

d²/ds² x(s) + k(s) x(s) = (1/ρ) (Δp/p)

where k(s) is a non-constant focusing force that encodes both strong and weak focusing, Δp/p is the relative momentum deviation from the design value, and ρ is the radius of curvature of the design path. This identifies the focusing system as a parametric oscillator, and its properties are worked out with ray transfer matrix analysis, the same mathematical tool used for lens systems in optics.

The full equations of motion come from relativistic Hamiltonian mechanics, almost always within the paraxial approximation, in which particles travel close to the design axis. When the magnetic fields are strongly nonlinear and the paraxial approximation fails, Lie transforms can still be used to build high-accuracy integrators of the equations.

## Modeling and beam diagnostics

Accurate modeling requires two linked steps: calculating the electric and magnetic fields produced by the accelerator elements, and tracking charged particles through those fields. Several specialized software packages exist for this, and Geant4 is a widely used tool for particle-matter interactions in accelerator contexts.

Beam diagnostics are the instruments that measure the real beam and decide whether the machine is working. Common devices include Beam Position Monitors (BPMs) for bunch position, fluorescent screens and Optical Transition Radiation (OTR) devices for imaging the transverse profile, wire scanners for the cross-section, and toroids or Integrating Current Transformers (ICTs) for the total bunch charge. The physics of each device is well understood, but designing one to make a reliable measurement on a specific machine is its own engineering problem, and the quality of a facility's diagnostics often determines whether the whole machine succeeds.

## Tolerances and tuning

No large accelerator is built perfectly. Component misalignment, small field-strength errors, and similar imperfections are inevitable, so physicists must know the tolerances within which a machine will still meet its design performance. Engineers supply expected tolerances for each component, and full physics simulations then predict behaviour under realistic errors. In many cases the simulated performance is unacceptable, and the fix is either to re-engineer the offending component or to add a tuning algorithm that steers the machine back to design. Because several error sources act at once, the chosen algorithms are typically validated in simulation across many error conditions before they are trusted on the real machine.

Source: adapted from "Accelerator physics" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Accelerator_physics

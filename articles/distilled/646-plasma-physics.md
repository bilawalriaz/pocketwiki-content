# Plasma (physics)

## Overview

Plasma is the fourth state of matter, formed when a gas undergoes sufficient ionization to contain a significant fraction of charged particles (ions and electrons). It is estimated that 99.9% of all ordinary matter in the universe is plasma, including stars, the interstellar medium, and the intracluster medium. Unlike solids, liquids, and gases, plasma is governed by collective electromagnetic interactions, making its behavior highly sensitive to external fields and giving rise to complex phenomena. Plasma physics is a major field of study with applications ranging from astrophysics to industrial manufacturing.

## Timeline

- **c. 1803** — Electric arc discovered independently by Vasily Petrov and Humphry Davy
- **1831** — Michael Faraday systematically investigates electric glow discharge in rarefied gases
- **1879** — Sir William Crookes suggests the idea of a fourth state of matter
- **1928** — Irving Langmuir introduces the term "plasma" for ionized gas

## Body

### Definitions and Classification

Plasma is an electrically conductive state of matter in which an ionized substance becomes dominated by long-range electric and magnetic fields. It is typically quasineutral, meaning the overall charge density is approximately zero, with electron and ion densities related by \( n_e = \langle Z_i \rangle n_i \), where \( \langle Z_i \rangle \) is the average ion charge. Plasma is distinct from a mere ionized gas; even low-density plasmas exhibit collective behavior governed by electromagnetic fields rather than simple kinetic motion.

An **ideal plasma** satisfies three criteria: (1) the plasma approximation, where the plasma parameter \( \Lambda \) (number of charge carriers in the Debye sphere) is much greater than unity; (2) the Debye length is much smaller than the system size, ensuring quasineutrality in the bulk; and (3) collisionlessness, where the electron plasma frequency exceeds the electron-neutral collision frequency.

**Non-neutral plasmas** have a significant charge imbalance, such as electron beams or plasmas in Penning traps. **Dusty plasmas** contain micron-sized dust particles that acquire high charges and interact strongly, often studied as complex plasmas under laboratory conditions.

### Properties and Parameters

The **degree of ionization** \( \alpha = \frac{n_i}{n_i + n_n} \) measures the fraction of ionized particles, where \( n_i \) is ion density and \( n_n \) is neutral density. Fully ionized matter has \( \alpha = 1 \). Plasma temperature, measured in kelvin or electronvolts, reflects thermal kinetic energy per particle. In thermal equilibrium, the Saha equation relates ionization degree to temperature and density. Non-thermal plasmas often exhibit separate electron and ion temperatures due to mass differences.

The **plasma potential** (or space potential) is the average electric potential within the plasma. Due to high conductivity, internal electric fields are small, but boundary regions like the **Debye sheath** near electrodes can have significant potentials. The Boltzmann relation \( n_e \propto \exp(e\Phi / k_B T_e) \) links electron density to potential, allowing calculation of electric fields via \( \vec{E} = \frac{k_B T_e}{e} \frac{\nabla n_e}{n_e} \).

**Magnetization** occurs when magnetic fields are strong enough to influence charged particle motion, typically when the electron gyrofrequency \( \nu_{ce} \) exceeds the collision frequency \( \nu_{coll} \). Magnetized plasmas are anisotropic, with properties differing parallel and perpendicular to the field. The electric field associated with a plasma moving with velocity \( \vec{v} \) in a magnetic field \( \vec{B} \) is given by \( \vec{E} = -\vec{v} \times \vec{B} \), and is not affected by Debye shielding.

### Mathematical Descriptions

Plasma behavior is described using either **fluid models** or **kinetic models**. Fluid models, such as magnetohydrodynamics (MHD), treat plasma as a continuum governed by Maxwell's equations and the Navier-Stokes equations. These are accurate when collisionality maintains a Maxwellian velocity distribution. **Kinetic models** track the velocity distribution function directly, necessary for collisionless plasmas. The **particle-in-cell (PIC)** method follows individual particle trajectories, while the **Vlasov equation** describes collisionless dynamics. In magnetized plasmas, **gyrokinetic** approaches reduce computational complexity.

### Plasma Science and Technology

Plasmas dominate astrophysical environments, including the solar wind, stellar interiors, accretion disks, and astrophysical jets (e.g., M87's jet extending ~5,000 light-years). Artificial plasmas are generated via electric or magnetic fields applied to gases, categorized by power source (DC, RF, microwave), pressure (vacuum, moderate, atmospheric), ionization degree (fully, partially, weakly), and temperature relationships (thermal vs. non-thermal).

Industrial applications include plasma etching in semiconductor manufacturing, plasma spraying for coatings, metal cutting and welding, and exhaust cleanup. Low-pressure discharges like glow discharges and capacitively coupled plasmas (CCP) are common in microfabrication. Atmospheric pressure discharges include arc, corona, and dielectric barrier discharges (DBD), the latter enabling plasma medicine and nanomaterial synthesis.

Magnetohydrodynamic (MHD) converters aim to convert plasma kinetic energy directly into electricity without moving parts. However, weakly ionized technological plasmas face challenges like the **electrothermal instability**, which limits performance in high Hall parameter regimes.

### Complex Plasma Phenomena

Plasma behavior exhibits extraordinary complexity due to nonlinear interactions. **Filamentation** produces striations in phenomena like lightning, solar flares, and laser-produced plasmas. High-power laser filamentation involves self-focusing and plasma defocusing, creating long plasma channels. **Impermeable plasma**, a thermal plasma acting as a solid barrier to gas, was briefly studied by a group led by Hannes Alfvén in the 1960s and 1970s for its possible applications in insulation of fusion plasma from the reactor walls. However, it was later found that the external magnetic fields in this configuration could induce kink instabilities in the plasma and subsequently lead to an unexpectedly high heat loss to the walls. In 2013, a group of materials scientists reported that they have successfully generated stable impermeable plasma with no magnetic confinement using only an ultrahigh-pressure blanket of cold gas.

## Terms

- **Plasma**: An ionized gas containing a significant fraction of charged particles, exhibiting collective electromagnetic behavior.
- **Quasineutrality**: The condition where the net charge density of a plasma is approximately zero over large volumes.
- **Debye length**: The characteristic length scale over which electric fields are screened in a plasma.
- **Plasma frequency**: The natural oscillation frequency of electrons in a plasma, given by \( \omega_{pe} = \sqrt{n_e e^2 / (\varepsilon_0 m_e)} \).
- **Magnetization**: The condition where magnetic fields significantly influence charged particle motion.
- **Thermal plasma**: A plasma where electrons, ions, and neutral gas share the same temperature.
- **Non-thermal plasma**: A plasma where electron temperature greatly exceeds ion and gas temperatures.
- **Particle-in-cell (PIC)**: A kinetic simulation method tracking individual particle trajectories in electromagnetic fields.
- **Magnetohydrodynamics (MHD)**: A fluid model treating plasma as a single conducting fluid governed by Maxwell's equations and fluid dynamics.
- **Degree of ionization**: The fraction of neutral particles that are ionized, \( \alpha = n_i / (n_i + n_n) \).

## Debates and Open Questions

The definition of plasma remains context-dependent: whether a given degree of ionization suffices to classify a substance as plasma depends on the phenomenon under study. The transition from gas to plasma is not a sharp phase transition but a gradual process, making the boundary between partially ionized gas and plasma a matter of interpretation. Additionally, the stability and scalability of advanced plasma technologies, such as MHD converters and impermeable plasmas, remain active areas of research due to instabilities and computational challenges.
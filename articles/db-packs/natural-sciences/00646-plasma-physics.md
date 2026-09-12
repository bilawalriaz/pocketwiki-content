# Plasma (physics)

A plasma is the fourth state of matter: a gas in which enough atoms have shed electrons to form free ions and free electrons that dominate the behaviour. Roughly 99.9% of the ordinary matter in the observable universe is plasma, including the matter inside stars, the diffuse gas between stars, and the hot gas that fills the space between galaxy clusters. Because charged particles respond to electric and magnetic forces, a plasma behaves collectively rather than as independent particles, and its behaviour is set by long-range electromagnetic fields rather than by short-range collisions.

## What makes a plasma a plasma

An ideal plasma satisfies three conditions. First, the plasma parameter, the number of charge carriers inside a Debye sphere, is much greater than one, so that many particles participate in screening any local charge imbalance. Second, the Debye length, the distance over which a plasma can screen out an electric field, is much smaller than the size of the system, so the bulk is quasineutral, with positive and negative charge densities nearly equal and related by $n_e = \langle Z_i \rangle n_i$, where $\langle Z_i \rangle$ is the average ion charge. Third, the plasma is effectively collisionless: the natural electron plasma frequency $\omega_{pe} = \sqrt{n_e e^2/(\varepsilon_0 m_e)}$ exceeds the rate at which electrons collide with neutral atoms.

These conditions separate a true plasma from a merely ionized gas. Even a low-density ionized gas that satisfies the criteria still displays collective oscillations, waves, and shielding that a weakly ionized gas does not. Plasmas with a significant charge imbalance, such as electron beams or plasmas in Penning traps, are called non-neutral plasmas, and dusty plasmas contain charged micron-sized particles that couple strongly to the surrounding ions and electrons.

## Key parameters

The degree of ionization $\alpha = n_i / (n_i + n_n)$ gives the fraction of particles that are ionized; $\alpha = 1$ describes fully ionized matter. In thermal equilibrium the Saha equation links this fraction to temperature and density. Because electrons are much lighter than ions, they respond to heating and fields far more quickly, so non-thermal plasmas often have an electron temperature far above the ion or neutral gas temperature, while a thermal plasma has electrons, ions, and neutrals at the same temperature.

The plasma potential is the average electric potential within the plasma. Internal electric fields are small because of high conductivity, but the Debye sheath, a thin boundary layer near any electrode, can carry a significant potential. The Boltzmann relation $n_e \propto \exp(e\Phi / k_B T_e)$ links electron density to potential, so electric fields follow the density gradient through $\vec{E} = (k_B T_e / e)(\nabla n_e / n_e)$.

A plasma is magnetized when a magnetic field is strong enough to bend charged-particle motion, generally when the electron gyrofrequency $\nu_{ce}$ exceeds the collision frequency $\nu_{coll}$. A magnetized plasma is anisotropic: motion along the field differs from motion across it. A plasma moving with velocity $\vec{v}$ through a magnetic field $\vec{B}$ generates an electric field $\vec{E} = -\vec{v} \times \vec{B}$, which is not screened by Debye shielding.

## Modelling plasma behaviour

Two broad families of models describe plasmas. Fluid models, including magnetohydrodynamics (MHD), treat the plasma as a conducting fluid governed by Maxwell's equations and the Navier–Stokes equations; they work well when collisions keep the velocity distribution close to Maxwellian. Kinetic models track the full velocity distribution, which is necessary for collisionless or non-thermal plasmas. The Vlasov equation describes collisionless dynamics, the particle-in-cell (PIC) method follows individual particle trajectories through self-consistent electromagnetic fields, and gyrokinetic methods reduce the cost of simulating magnetized plasmas by averaging over the fast gyration of particles around field lines.

## Generating and using plasmas

Artificial plasmas are created by applying electric or magnetic energy to a gas and are classified by the power source (DC, radio-frequency, microwave), the pressure (vacuum, moderate, atmospheric), the degree of ionization, and whether the plasma is thermal or non-thermal. Industrial uses include plasma etching in semiconductor manufacturing, plasma spraying for wear-resistant coatings, welding, metal cutting, and exhaust treatment. Low-pressure discharges such as glow discharges and capacitively coupled plasmas are workhorses of microfabrication, while atmospheric discharges including arcs, coronas, and dielectric barrier discharges support applications in plasma medicine and nanomaterial synthesis.

A long-standing proposal is the magnetohydrodynamic (MHD) converter, which would let plasma flow past electrodes to generate electricity directly, without moving parts; in practice, weakly ionized technical plasmas suffer from the electrothermal instability, which limits performance in regimes with a high Hall parameter.

## Complex behaviour and open questions

Plasmas are nonlinear systems, and the same filamentation pattern that gives lightning its branched structure also appears in solar flares and in the channels carved by high-power laser pulses, where self-focusing and plasma defocusing balance to produce long, narrow plasma filaments. In the 1960s and 1970s, a group led by Hannes Alfvén explored "impermeable plasma", a thermal plasma dense enough to act as a solid barrier, with the hope of insulating fusion plasma from reactor walls; the concept was undermined when the required external magnetic fields were found to drive kink instabilities that funnelled heat to the walls. In 2013, materials scientists reported generating stable impermeable plasma without magnetic confinement, using only an ultrahigh-pressure blanket of cold gas.

No single definition draws a sharp line between a weakly ionized gas and a plasma, and the threshold for calling something a plasma depends on which collective phenomenon is being studied. The transition is gradual rather than a true phase transition, and the stability and scalability of devices such as MHD converters and impermeable-plasma systems remain active research problems.

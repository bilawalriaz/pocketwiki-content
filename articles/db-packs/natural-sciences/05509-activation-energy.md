# Activation energy

In the Arrhenius model of reaction rates, **activation energy (Eₐ)** is the minimum energy barrier that reactant molecules must overcome to convert into products. A reaction proceeds only when enough molecules carry kinetic energy at or above this barrier, which is why most reactions need sufficient temperature. The term was introduced in 1889 by the Swedish scientist Svante Arrhenius, and Eₐ is measured in kJ/mol or kcal/mol.

## The Arrhenius equation

The rate of a reaction is tied to Eₐ by the Arrhenius equation:

$$k = A e^{-E_a / (RT)}$$

where k is the rate constant, A is the pre-exponential factor (a constant that reflects how often molecules collide with the right orientation), R is the gas constant, and T is absolute temperature in kelvins. Because Eₐ sits in a negative exponent, small changes in Eₐ or T cause large changes in k. Eₐ can be measured experimentally by recording how k changes with T, even when A is unknown.

A caution: the Eₐ extracted this way is an experimentally fitted parameter describing temperature sensitivity, not a direct measurement of one barrier. Bulk experiments average over billions of collisions with varied geometries, angles, and energies, and most reactions proceed through several elementary steps, each with its own barrier. The fitted Eₐ is an average across all of them and has limited theoretical meaning as a single threshold.

## Catalysts and the transition state

The **transition state** is the high-energy, unstable arrangement of atoms at the top of the barrier, partway between reactants and products. A **catalyst** is a substance that lowers Eₐ by stabilising this transition state. Catalysts, including protein-based ones called **enzymes** (which may use small-molecule cofactors), are not consumed and do not change the energies of the starting materials or products, so they cannot shift a reaction's equilibrium, only the speed at which it is reached.

The catalytic effect comes from binding energy. When a substrate slots into an enzyme's active site, hydrogen bonds, van der Waals forces, and other stabilising interactions release energy. This released energy, called the binding energy, helps push the substrate up into the high-energy transition state, so less external energy from heat is required. A non-catalysed reaction lacks this free-energy assistance and so needs more energy to reach the same transition state.

## Gibbs energy of activation

Transition state theory refines the picture with the **Eyring equation**:

$$k = \frac{k_B T}{h} e^{-\Delta G^\ddagger / (RT)}$$

Here k_B and h are the Boltzmann and Planck constants, and **ΔG‡** is the Gibbs energy of activation, the free-energy cost of reaching the transition state. Because ΔG‡ = ΔH‡ − TΔS‡, it includes an entropic contribution that the Arrhenius form hides inside A. For a one-step unimolecular reaction, Eₐ ≈ ΔH‡ + RT and A ≈ (k_BT/h) exp(1 + ΔS‡/R), but A in proper Arrhenius theory is temperature-independent, while the Eyring version carries a linear T dependence. For a one-step process with a half-life near 2 hours at room temperature, ΔG‡ is about 23 kcal/mol, roughly the same magnitude as Eₐ.

In practice, because TΔS‡ and RT are small at ordinary temperatures, Eₐ, ΔG‡, and ΔH‡ are often used interchangeably in informal discussion, even though they are distinct quantities. The overall free-energy change of a reaction (whether exergonic or endergonic) is independent of Eₐ; Eₐ controls rate, not whether a reaction is spontaneous.

## Negative activation energy

Some reactions slow down as temperature rises, giving a fitted Eₐ below zero. Two mechanisms produce this.

**Barrierless elementary reactions** have no genuine barrier to climb. Instead, reaction depends on two molecules being captured in a **potential well**, a region where attractive forces trap them close together long enough to react. As T rises, colliding molecules carry more momentum and are more likely to glance past rather than stick, so the **reaction cross-section** (the effective target area for a productive collision) shrinks with temperature. The rate falls even though no barrier exists.

**Multistep reactions** can also show an apparent negative Eₐ. If a rapid pre-equilibrium (an initial fast step that settles into a balance between reactants and an intermediate) whose constant drops sharply with T precedes a slow step, the drop in the equilibrium concentration of the intermediate can outweigh the speeding-up of the slow step, and the overall rate falls with T. The termolecular oxidation 2 NO + O₂ → 2 NO₂ is one example, with rate law v = k[NO]²[O₂] and a negative Eₐ, explained by the two-step mechanism 2 NO ⇌ N₂O₂ followed by N₂O₂ + O₂ → 2 NO₂.

Cationic chain-growth polymerisations can also show a negative overall Eₐ = Eᵢ + Eₚ − Eₜ. Because the propagation step has a very small Eₐ of its own, the overall value becomes negative when the termination step has a larger Eₐ than initiation; typical values lie between 40 and 60 kJ/mol.

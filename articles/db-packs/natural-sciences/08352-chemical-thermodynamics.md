# Chemical thermodynamics

Chemical thermodynamics asks one central question: given a mixture of substances, can a proposed reaction or phase change actually happen, and if so, under what conditions? It answers that question by combining the laws of energy and entropy into a small set of state functions whose signs and magnitudes predict spontaneity, equilibrium, and the maximum work a process can deliver.

A **state function** is a property whose value depends only on the current state of the system, not on how that state was reached. The framework rests on four of them. **Internal energy** (U) is the total energy locked in a system's molecular motions and bonds. **Enthalpy** (H) is U plus the pressure–volume work needed to make room for the system at constant pressure, so it is the natural quantity for reactions in open vessels. **Entropy** (S) measures how many microscopic arrangements a macroscopic state hides; it increases in every spontaneous process. **Gibbs free energy** (G) is the combination H − TS and, at constant temperature and pressure, its decrease equals the maximum useful work a process can produce, with the rest dissipated as heat.

The three global statements the subject relies on are: the energy of the universe is constant; any spontaneous process increases the entropy of the universe; and a perfect crystal at 0 K has zero entropy. From the first two, four "fundamental equations of Gibbs" can be derived, and from those the entire mathematical apparatus follows by routine calculus.

A reaction's energy change is the difference between the bond energies of products and reactants. At constant volume, the heat measured equals ΔU; at constant pressure, it equals ΔH, the enthalpy change, which is why tables list enthalpies of formation rather than internal energies. The reaction of potassium with water, which releases enough chemical energy to produce heat and a lilac flame, shows a large negative enthalpy converted into heat and light.

The workhorse equation for most laboratory chemistry is the differential of G at constant T and P:

(dG)_{T,P} = Σ_i μ_i dN_i

Here μ_i is the **chemical potential** of species i, defined as (∂G/∂N_i) at fixed T, P, and all other N_j. Chemical potential is **intensive**, meaning it does not scale with the size of the system, and depends only on the local molecular neighbourhood, so it can be evaluated at any point inside a system, not just in a uniform bulk phase. Two phases at the same T and P sit in equilibrium when each chemical potential matches across the boundary, which is the condition that governs phase equilibrium and diffusion.

Because molecules cannot appear or disappear independently (mass and atoms are conserved), a better variable is the **extent of reaction** ξ, which advances by one unit when the reaction completes one stoichiometric turn. The stoichiometric coefficient ν_i = ∂N_i/∂ξ is negative for reactants and positive for products. With this change of variable, the same differential becomes

(dG)_{T,P} = −A dξ

where the **affinity** A, a concept introduced by Théophile de Donder in 1923, is Σ_i μ_i ν_i. The minus sign is chosen so that spontaneous reactions have A > 0: Gibbs energy falls, entropy is produced, and the species in effect attract each other. For several reactions running in parallel,

(dG)_{T,P} = −Σ_k A_k dξ_k,  and at every instant  A_k · (dξ_k/dt) ≤ 0,

a purely local criterion that holds even though the chemical potentials themselves cannot "know" whether T and P will stay fixed. At equilibrium every A_k is zero.

In practice, chemists rarely write A and ξ. Instead they use ΔG (in molar units) as a shorthand for ∂G/∂ξ and state the rule that all spontaneous reactions have a negative ΔG, a restatement of the second law dressed in units of energy rather than entropy, valid only when no useful work is being extracted. When work is captured, it must be subtracted from the Gibbs decrease; any leftover appears as heat, which is T times an entropy increase in the surroundings.

Reactions are usually coupled to mechanical or electrical constraints. A gas-producing reaction in a piston can advance only as the piston retreats, and pushing the piston back drives the reaction in reverse. A redox reaction in a battery delivers current only because the electrodes are wired; disconnect the wire and the reaction may still trickle on, leaking free energy as Joule heat. A rechargeable lead–acid cell reverses the same chemistry by forcing current backwards. In biology, the hydrolysis of ATP to ADP and phosphate is the canonical example: it is not an independent process but is coupled through cellular machinery to the force-and-distance work of a contracting muscle, while synthesis of ATP in mitochondria and chloroplasts is in turn driven by a redox chain that pumps ions across membranes. Coupling is rarely perfect; a coupling coefficient describes what fraction of the Gibbs decrease becomes external work versus heat or side reactions.

Conventional chemical thermodynamics treats systems at or very near equilibrium. Far from equilibrium, the subject opens into non-equilibrium thermodynamics, developed largely by Ilya Prigogine. He showed that open systems driven by sustained energy exchange can self-organise into ordered, stable patterns he called **dissipative structures**, which exist only as long as the exchange continues. The same mathematics has been applied to city traffic, insect communities, the development of biological form, and the growth of tumours, settings where classical near-equilibrium theory predicts only disorder.
```

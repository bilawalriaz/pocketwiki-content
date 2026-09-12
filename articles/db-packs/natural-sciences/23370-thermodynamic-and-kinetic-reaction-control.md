# Thermodynamic and kinetic reaction control

When two reaction pathways lead to different products from the same starting materials, the product ratio depends on whether the faster pathway or the more stable product dominates. The pathway that forms first is the **kinetic product**; the pathway that gives the lowest-energy product is the **thermodynamic product**. Temperature, solvent, pressure, and reaction time decide which one wins. Selectivity between the two arises only when the two pathways have different **activation energies** (the minimum energy a molecule must have to react), so that one rate is faster than the other.

## Working model

A reaction coordinate is a plot of energy against progress along the reaction path, with peaks for transition states (short-lived, high-energy arrangements of atoms through which bonds break and form) and valleys for intermediates or products. Product A sits behind a lower barrier; product B sits in a deeper well.

- Kinetic control: the reaction is short or cold, so only the first-formed product accumulates. The product ratio tracks the ratio of rate constants, which depends on the gap between activation energies.
- Thermodynamic control: the reaction is long or hot enough for products to interconvert, so the system reaches equilibrium. The product ratio tracks the difference in **Gibbs free energy** (the energy available to do work at constant temperature and pressure) between products.

Both regimes lie on a continuum set by temperature and time scale. The first product formed in any reaction is the one formed most easily, so every reaction begins under kinetic control. Whether it stays there depends on whether equilibration is fast enough on the experimental time scale.

## Quantitative form

For two competing products A and B at fixed reaction time, the kinetic ratio is

ln([A]/[B]) = −ΔEₐ / RT

where ΔEₐ is the difference in activation energies, R the gas constant, and T the temperature. This comes from the Arrhenius rate law (a relation stating that a rate constant grows exponentially with temperature divided by activation energy).

Once equilibrium is reached, the thermodynamic ratio is

ln([A]∞/[B]∞) = −ΔG° / RT

where ΔG° is the difference in standard Gibbs free energy of the two products, and the ratio equals the equilibrium constant K_eq.

In practice, "pure" kinetic control requires that equilibration be negligible during the reaction, and "pure" thermodynamic control requires an effectively infinite reaction time. Both are idealizations, but most real systems approximate one or the other.

## General trends

- Low temperature increases selectivity under either regime, because T sits in the denominator of both equations.
- The fastest-forming product is best prepared at the lowest temperature that still gives a workable rate.
- The most stable product is best prepared at the lowest temperature that still allows equilibrium to be reached in a reasonable time, then slowly cooling the mixture to shift equilibrium further toward the stable product.
- A large stability gap lets the thermodynamic product dominate even under fairly vigorous conditions.
- Thermodynamic control at a given temperature implies thermodynamic control at any higher temperature for the same reaction time; kinetic control at a given temperature implies kinetic control at any lower temperature.
- A change in product ratio with temperature that exceeds the change predicted by the kinetic equation signals equilibration, that is, thermodynamic control. A change inconsistent with the thermodynamic equation signals kinetic control.

## Worked examples

**Diels–Alder reaction of cyclopentadiene with furan.** Two isomers form. At room temperature the less stable *endo* isomer dominates because its transition state benefits from favorable orbital overlap. At 81 °C over long reaction times the *exo* isomer dominates because it has less steric congestion (atoms pushing against each other for space). The exo product is the thermodynamic product; the endo product is the kinetic product.

**Protonation of an enolate.** Enolate ions (negatively charged forms of carbonyl compounds, with the charge delocalized over oxygen and carbon) and the protonated keto and enol forms interconvert via fast proton transfers. Under kinetic control the enol, the less stable tautomer (a structural isomer that differs only in the position of a hydrogen and a double bond), forms first. Under thermodynamic control the keto form predominates because the C=O bond is stronger than the C=C bond. Deprotonation of an unsymmetrical ketone gives either the less substituted (kinetic, from removal of the most accessible α-hydrogen, a hydrogen on the carbon next to the carbonyl) or the more substituted enolate (thermodynamic, more substituted alkenes are more stable). Low temperature and a sterically hindered base favor the kinetic enolate.

**Electrophilic addition of HBr to 1,3-butadiene.** Above room temperature the 1,4-adduct (1-bromo-2-butene) predominates because its internal double bond is more substituted and more stable. Below room temperature the 1,2-adduct (3-bromo-1-butene) predominates because protonation follows Markovnikov's rule (the proton adds to the carbon already bearing more hydrogens), placing positive charge on the more substituted carbon, which is then captured fastest by bromide.

## Asymmetric synthesis

Pairs of enantiomers (nonsuperimposable mirror-image molecules) have essentially identical Gibbs free energy, so thermodynamic control gives a racemic mixture (equal amounts of both enantiomers). Any catalytic reaction that produces nonzero enantiomeric excess (a measure of how much one enantiomer exceeds the other) operates under at least partial kinetic control. Many stoichiometric asymmetric reactions form the product as a diastereomeric complex (a non-mirror-image stereoisomer of the complex) with the chiral auxiliary (a temporary chiral group used to steer the stereochemistry) before workup and still fall under kinetic control, although thermodynamic control is in principle possible.

## Detection of regime

To test which regime a new reaction occupies, vary the temperature and reaction time. A product distribution that changes with time, inverts with temperature, or shifts more than the kinetic equation predicts indicates equilibration and thermodynamic control. A distribution that shifts more than the thermodynamic equation predicts indicates kinetic control.

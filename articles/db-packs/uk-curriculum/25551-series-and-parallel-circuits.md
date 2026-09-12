# Series and parallel circuits

Two-terminal components—resistors, capacitors, inductors, switches, cells—can be connected in series (along a single electrical path) or in parallel (along multiple paths). The distinction governs how current and voltage distribute, how total resistance, capacitance, and inductance combine, and whether a failure in one component disables the whole network.

In a series connection, the same current flows through every component. The voltage across the network equals the sum of the voltage drops across each component. Opening the circuit at any point stops all current. In a parallel connection, the same voltage appears across every component. The total current equals the sum of the branch currents. Each component has its own path to the source, so one can fail while others continue operating.

**Current and voltage relationships**

Series: I = I₁ = I₂ = … = Iₙ; V = ΣVᵢ = I ΣRᵢ  
Parallel: V = V₁ = V₂ = … = Vₙ; I = ΣIᵢ = V Σ(1/Rᵢ)

These two statements are duals, exchanging the roles of voltage and current.

**Resistance and conductance**

For resistors in series, resistances add directly: R = R₁ + R₂ + … + Rₙ. For resistors in parallel, add the reciprocals and take the reciprocal of the sum: R = (1/R₁ + 1/R₂ + … + 1/Rₙ)⁻¹. The total parallel resistance is always less than the smallest individual resistance. For two resistors this simplifies to the product-over-sum rule: R = R₁R₂/(R₁+R₂). For N equal resistors R′ in parallel, R = R′/N.

Conductance G = 1/R behaves oppositely: series conductances combine like parallel resistances, and parallel conductances add directly. G_series = (1/G₁ + 1/G₂ + …)⁻¹; G_parallel = G₁ + G₂ + ….

**Capacitors and inductors**

Capacitors in series combine like resistors in parallel: C = (1/C₁ + 1/C₂ + …)⁻¹. In parallel they add directly: C = C₁ + C₂ + …. The working voltage of a parallel capacitor bank is limited by the lowest-rated capacitor.

Inductors in series add directly: L = L₁ + L₂ + …, provided their magnetic fields do not couple. In parallel they combine like resistors in parallel: L = (1/L₁ + 1/L₂ + …)⁻¹, again assuming no mutual coupling. When mutual inductance M exists between two coils, the equivalent inductance depends on field orientation. For two inductors L₁ and L₂ with mutual inductance M in series, the total is L₁ + L₂ ± 2M; for equal inductors L this becomes 2(L ± M). In parallel, two equal tightly coupled coils yield L ≈ (L + M)/2; if one coil is reversed so M is negative, the combination becomes nearly non-inductive. With unequal tightly coupled inductors, near short-circuit conditions and high circulating currents can arise. For more than two coupled inductors, matrix methods are required.

**Switches and cells**

Switches in series implement logical AND: current flows only if all are closed. Switches in parallel implement logical OR: current flows if any is closed.

Cells in series add their voltages: a 12 V car battery contains six 2 V cells in series; two 12 V batteries in series give 24 V. Cells in parallel share the same voltage as a single cell but divide the total current. Four identical cells in parallel delivering 1 A total supply 0.25 A each. Non-identical cells in parallel will attempt to charge each other, risking damage. Parallel-connected batteries increase ampere-hour capacity: laptop lithium-ion packs and solar storage systems use this arrangement.

**Notation**

The parallel operator ∥ (two vertical lines) compactly expresses parallel combinations: R₁ ∥ R₂ = (R₁⁻¹ + R₂⁻¹)⁻¹ = R₁R₂/(R₁+R₂). It extends naturally: R₁ ∥ R₂ ∥ R₃ = R₁R₂R₃/(R₁R₂ + R₁R₃ + R₂R₃).

**Applications**

Series circuits raise voltage: disposable zinc cells in series power a 3 V flashlight; a dozen lithium-ion cells in series give 48 V for a power tool. Early electric trains used series strings of lamps (eight 70 V bulbs on a 600 V line) with a series resistor to drop excess voltage, later replaced by motor-generators and solid-state devices. In physiology, blood vessels within an organ—artery, arterioles, capillaries—form a series resistance network where arterioles contribute the largest share.

Parallel circuits increase current capacity and redundancy. The circulatory system illustrates parallel resistance: arteries branching from the aorta give total resistance 1/R_total = 1/R_a + 1/R_b + …, always less than any individual artery. Parallel battery banks in portable radios, laptops, and solar installations sum ampere-hour ratings while maintaining cell voltage.

# Single-molecule magnet

A single-molecule magnet (SMM) is a metal-organic compound that holds a stable magnetization below a blocking temperature, showing magnetic hysteresis of purely molecular origin. Unlike bulk magnets, no long-range ordering of magnetic moments is needed; each molecule is an independent nanoscale magnet.

The first SMM, [Mn₁₂O₁₂(OAc)₁₆(H₂O)₄] ("Mn₁₂"), was reported in 1991, the term "SMM" came in 1996. It contains a central Mn(IV)₄O₄ cube surrounded by eight Mn(III) ions bridged by oxo ligands, with slow relaxation up to about 4 K. Mn₁₂ set the template for a field whose goal is to raise operating temperatures toward liquid nitrogen (77 K) or room temperature for magnetic memory.

## Why the magnetization holds

Magnetic anisotropy (a preferred axis) gives an SMM two stable orientations, antiparallel and separated by an energy barrier. At low temperature, thermal fluctuations rarely flip the moment; above the blocking temperature, flips become fast and the molecule looks paramagnetic. The picture is the same superparamagnetic behavior as in small magnetic particles, applied at the molecular level.

The average time between flips, the Néel relaxation time τ, follows the Néel–Arrhenius law:

τ⁻¹ = τ₀⁻¹ exp(−U_eff / k_B T)

U_eff is the effective barrier (reported in cm⁻¹ or K), τ₀ is a material-specific attempt time (~10⁻⁹–10⁻¹⁰ s), k_B is Boltzmann's constant, T is temperature. τ ranges from nanoseconds to years. Three ingredients produce a large barrier: a high total ground-state spin from ferromagnetic coupling of metal-ion spins (mediated by superexchange through bridging ligands), strong magnetic anisotropy (zero-field splitting), and weak intermagnetic interaction between molecules.

Intramolecular spin coupling follows the Heisenberg Hamiltonian H = −Σᵢ<ⱼ Jᵢ,ⱼ Sᵢ·Sⱼ: positive J is ferromagnetic (parallel spins), negative J is antiferromagnetic. Designing SMMs means choosing metals and ligands that maximize both spin and anisotropy.

## Measuring performance

Two quantities define performance:

- Blocking temperature T_B, the temperature at which τ equals 100 s. The 100-s figure is a comparison standard, not a physical threshold.
- Effective barrier U_eff. T_B and U_eff track each other only when relaxation is purely Arrhenius.

The average T_B across known SMMs is about 4 K. Dysprosium metallocenium salts dominate the high-temperature records: dysprosocenium reached 56 K in 2017, 59–67 K in 2018, and 80 K hysteresis in 2018, because Dy(III) combines large spin with strong single-ion anisotropy. Mn₁₂ reaches only ~3 K with U_eff ≈ 42 cm⁻¹; the best dysprosocenium salts reach U_eff ~1200–1540 cm⁻¹ with T_B of 50–80 K. Iron clusters (Fe₈, Fe₄ cubes) and Mn₄ clusters are also studied. The Fe(II) cube [Fe₄(sae)₄(MeOH)₄] was the first Fe(II) SMM and shows non-collinear magnetism, with spin moments along two nearly perpendicular axes.

## Applications

Because each molecule could in principle store one bit and act as a qubit, SMMs are explored as ultra-thin hard-disk coatings, molecular memory cells (including Mn₁₂ patterned on polymers for DVD-style transfer), and quantum-computing building blocks. Calculations by Leuenberger and Loss showed Mn₁₂ and Fe₈ crystals implementing the Grover search algorithm with retrieval times near 10⁻¹⁰ s. Electric-field gating of Fe₄ SMMs switches between neutral and anionic states on short timescales, potentially above T_B. Machine-learning screens have proposed Cr₂Gd₂(OAc)⁺₅ and Fe₄Gd₆ clusters as magnetocaloric refrigerants with large entropy changes. SMMs also serve as test beds for quantum mechanics: macroscopic quantum tunneling of magnetization was first observed in Mn₁₂ as evenly spaced steps in the hysteresis loop, and quantum-phase interference in Fe₈ is explained by geometric (Berry) phase theory.

The remaining obstacle is temperature: the best dysprosium metallocenium SMMs just exceed the boiling point of liquid nitrogen, still far below room temperature, and higher U_eff and T_B remain the central targets for moving molecular magnets from laboratory curiosities into working memory and quantum devices.

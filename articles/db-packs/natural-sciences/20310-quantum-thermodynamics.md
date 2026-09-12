# Quantum thermodynamics

Quantum thermodynamics studies how the laws of thermodynamics emerge from quantum mechanics, with emphasis on small systems and processes far from equilibrium. Its seed was a 1905 argument by Einstein: reconciling thermodynamics with electromagnetism forces light into quanta of energy E = hν. The first university course, MIT 2.47J, was taught in 1971 by Hatsopoulos and Gyftopoulos.

The starting assumption is that the universe is a large closed quantum system evolving unitarily. A subsystem S coupled to a bath B has global Hamiltonian H = H_S + H_B + H_SB. The system's state is the reduced density matrix ρ_S(t) = Tr_B(ρ_SB(t)). Under weak coupling and the Markov property, the bath carries no memory of the system, and the equation of motion is the Lindblad (GKSL) equation:

ρ̇_S = −(i/ℏ)[H_S, ρ_S] + L_D(ρ_S)

The first term generates unitary evolution under H_S. The dissipator L_D encodes bath-induced energy exchange and drives ρ_S toward a steady state as t → ∞. For thermodynamics to hold, L_D must commute with H_S so the steady state is the Gibbs state at the bath's temperature, and the dynamics satisfies the KMS detailed-balance condition. Choosing H_S and L_D independently is a trap: arbitrary combinations can violate the second law.

Setting O = H_S in the Heisenberg equation yields the first law:

dE/dt = ⟨∂H_S/∂t⟩ + ⟨L_D*(H_S)⟩

The first term is power from time-dependent control; the second is heat current J to the bath.

The second law appears as irreversibility. For N coupled heat baths in steady state, the Clausius inequality ∑ J_n/T_n ≥ 0 holds, and Spohn's inequality gives a dynamical version for any GKSL generator. Local master equations for coupled networks were once claimed to break the second law, but a 2018 analysis showed that accounting for all work and energy contributions in the full system restores consistency.

Quantum adiabatic processes require [H(t), H(t')] = 0 so populations of instantaneous energy levels stay fixed. Violating this costs extra work. For an isolated system the extra work is recoverable, but bath-induced dephasing, a loss of phase coherence across energy eigenstates, makes it unrecoverable. This lost energy is quantum friction; shortcuts to adiabaticity have suppressed it experimentally in a unitary Fermi gas in a time-dependent trap.

The third law has two Nernst formulations. The heat theorem states that the entropy of any pure substance in equilibrium approaches zero as T → 0. The unattainability principle states that no finite procedure reaches absolute zero. Non-negative entropy production at the cold bath requires Ṡ_c ∝ −T_c^α with α ≥ 0; the heat theorem tightens this to α > 0, forcing Ṡ_c = 0 at T_c = 0 and scaling J_c ∝ T_c^(α+1). With heat capacity c_V ∼ T_c^η, the cooling exponent ζ = α − η + 1 governs approach to zero, and ζ < 0 would imply finite-time cooling to absolute zero, so the unattainability principle is the stronger constraint.

Two broader themes unify the field. Typicality, formalised by von Neumann's quantum ergodic theorem, says that almost every pure state in a large Hilbert space evolves so its expectation values match the ensemble average, so thermodynamic behaviour emerges without an averaging postulate. Resource theory recasts the laws as monotonicity statements about generalised free energies, extending them to few-particle systems and producing families of second-law constraints.

Recent work relaxes the assumption that conserved charges commute. Noncommuting charges invalidate standard thermal-state derivations, increase entanglement, can trigger critical dynamics, alter entropy production, and conflict with the eigenstate thermalisation hypothesis. Engineered reservoirs built with quantum coherence or nonthermal statistics can exceed classical efficiency limits, violate Clausius inequalities, or deliver simultaneous heat and work extraction.

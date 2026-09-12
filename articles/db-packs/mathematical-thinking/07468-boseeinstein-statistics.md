# Bose–Einstein statistics

Bose–Einstein (B–E) statistics describes how a collection of identical, non-interacting particles called bosons distributes itself across the available energy states of a system at thermal equilibrium. The defining feature is that there is no limit on how many bosons can occupy a single quantum state, so particles are free to pile into the lowest available levels. This concentration accounts for the coherent beam of laser light, the frictionless flow of superfluid helium, and the Bose–Einstein condensate first produced in 1995. Satyendra Nath Bose introduced the statistics for photons in 1924, and Albert Einstein extended it to atoms in 1924–25.

Bosons are particles with integer spin. Fermions, the contrasting case, have half-integer spin and obey the Pauli exclusion principle, which forbids more than one fermion per quantum state; their statistics is Fermi–Dirac. B–E statistics matters when quantum effects are significant, meaning the particle density N/V meets or exceeds the quantum concentration n_q, at which the average interparticle spacing equals the thermal de Broglie wavelength. At high temperature or low density both B–E and Fermi–Dirac reduce to the classical Maxwell–Boltzmann distribution.

## The distribution

The expected occupancy of energy level i is

n̄_i = g_i / (exp[(ε_i − μ)/k_B T] − 1),

where g_i is the degeneracy (the number of distinct sublevels sharing energy ε_i), μ is the chemical potential (zero for a photon gas), k_B is Boltzmann's constant, and T is the absolute temperature. The constraint ε_i > μ keeps the denominator positive, which for a fixed-number boson gas forces μ < 0 overall.

The minus one, rather than the plus one in Fermi–Dirac, is what lets n̄_i grow without bound as ε_i approaches μ. The variance of the count on a level is σ² = n̄(n̄ + 1), with standard deviation roughly equal to the mean, a consequence of the underlying geometric distribution of occupancy whose most probable value at any level is actually zero.

## Limits and connections

In the high-temperature or low-density limit, the exponential in the denominator is much larger than one, the ±1 in either quantum formula becomes negligible, and both statistics collapse to Maxwell–Boltzmann, n̄_i ≈ (g_i/Z) exp[−(ε_i − μ)/k_B T]. For low-energy states with ε_i − μ ≪ k_B T, the exponential expands to give n̄_i ≈ g_i k_B T/(ε_i − μ), the Rayleigh–Jeans form. For photons in equilibrium with matter, particle number is not conserved, so μ = 0 and the formula reproduces the Planck blackbody spectrum.

## Origin of the counting rule

The combinatorial heart of B–E statistics is the count of distinguishable arrangements. Placing n_i indistinguishable bosons into g_i sublevels of equal energy, with no upper limit per sublevel, yields

w_i = (n_i + g_i − 1)! / (n_i! (g_i − 1)!).

A useful picture: line up n identical balls and g − 1 movable dividers; the number of distinct orderings of these n + g − 1 objects is the same multinomial. Total microstates multiply across levels, W_BE = ∏ w_i. Maximising ln W subject to fixed N and E with Lagrange multipliers reproduces the distribution above, with β = 1/(k_B T) and α = −μ/(k_B T). The grand canonical ensemble reaches the same answer by summing a geometric series of single-state partition functions, which converges only when μ < ε for every state.

The discovery hinged on a similar indistinguishability argument: if coins behaved like bosons, the probability of two heads would be one-third rather than the one-quarter of classical coins, because the two "heads" outcomes are counted as a single arrangement.

## Where the rule shows up

B–E statistics governs photons, phonons, and helium-4 atoms in thermal equilibrium, and is the prerequisite for Bose–Einstein condensation, a phase transition in which a macroscopic fraction of bosons collapses into the single lowest quantum state below a critical temperature. The same distribution has been adopted in information retrieval as a "Divergence From Randomness" term-weighting model, and in network science it describes condensation-like phenomena such as winner-takes-all dynamics in growing networks.

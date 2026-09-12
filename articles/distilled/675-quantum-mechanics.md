# Quantum mechanics

## Overview

Quantum mechanics is the fundamental physical theory describing matter and light at atomic and subatomic scales, where classical physics fails. It provides probabilistic predictions via wave functions and probability amplitudes, and underpins technologies from lasers to semiconductors. Its development in the early 20th century revolutionized our understanding of nature and enabled entire fields such as quantum chemistry, quantum computing, and quantum information science.

## Timeline

- **c. 1900** — Max Planck solves black-body radiation by quantizing energy as \( E = h\nu \)
- **1905** — Albert Einstein explains the photoelectric effect using light quanta (photons)
- **1913** — Niels Bohr models the hydrogen atom with quantized electron orbits
- **1923** — Louis de Broglie proposes wave-particle duality for matter
- **1925** — Werner Heisenberg, Max Born, and Pascual Jordan develop matrix mechanics
- **1925** — Erwin Schrödinger formulates wave mechanics
- **1926** — Born introduces the probabilistic interpretation of the wave function
- **1927** — Quantum mechanics gains wider acceptance at the Fifth Solvay Conference
- **1935** — Einstein, Podolsky, and Rosen publish the EPR paradox
- **1964** — John Bell proves Bell's theorem, constraining local hidden variable theories

## Body

### Fundamental Concepts and Mathematical Formulation

Quantum mechanics describes physical systems using a mathematical framework rooted in Hilbert spaces. The state of a system is represented by a normalized vector \( \psi \) in a complex Hilbert space \( \mathcal{H} \), defined up to a global phase \( e^{i\alpha} \). Observables—physical quantities like position, momentum, and energy—are represented by Hermitian (self-adjoint) linear operators acting on this space. A quantum state may be an eigenstate of an observable, yielding a definite eigenvalue upon measurement, or a superposition of eigenstates.

The Born rule assigns probabilities to measurement outcomes: the probability of obtaining eigenvalue \( \lambda \) is \( |\langle \vec{\lambda}, \psi \rangle|^2 \) in the non-degenerate case, or \( \langle \psi, P_\lambda \psi \rangle \) using the projector \( P_\lambda \) onto the eigenspace in the degenerate case. Upon measurement, the wave function collapses to the corresponding eigenstate. Time evolution is deterministic and governed by the Schrödinger equation:

\[
i\hbar \frac{\partial}{\partial t} \psi(t) = H \psi(t),
\]

where \( H \) is the Hamiltonian operator representing total energy. The solution is \( \psi(t) = e^{-iHt/\hbar} \psi(0) \), with the time-evolution operator \( U(t) = e^{-iHt/\hbar} \) being unitary.

### Key Phenomena

The uncertainty principle arises from non-commuting observables. For position \( \hat{X} \) and momentum \( \hat{P} \), the canonical commutation relation \( [\hat{X}, \hat{P}] = i\hbar \) implies \( \sigma_X \sigma_P \geq \hbar/2 \). This generalizes to any pair of observables \( A \) and \( B \): \( \sigma_A \sigma_B \geq \frac{1}{2}|\langle [A,B] \rangle| \). Position and momentum are Fourier transforms of each other, linking uncertainty to wave packet spreading.

Quantum interference, demonstrated in the double-slit experiment, reveals wave-particle duality: particles produce interference patterns when unobserved, but behave as classical particles when measured. Quantum tunneling allows particles to traverse potential barriers classically forbidden, enabling phenomena like radioactive decay and technologies such as scanning tunneling microscopy.

Entanglement occurs when composite systems cannot be described by individual states alone. The joint Hilbert space is the tensor product \( \mathcal{H}_{AB} = \mathcal{H}_A \otimes \mathcal{H}_B \), and entangled states (e.g., \( \frac{1}{\sqrt{2}}(\psi_A \otimes \psi_B + \phi_A \otimes \phi_B) \)) defy separable descriptions. Entanglement enables quantum computing and communication protocols like quantum key distribution, though it does not permit faster-than-light signaling (no-communication theorem). Bell's theorem and subsequent tests have ruled out local hidden variable theories.

### Applications and Examples

Quantum mechanics explains microscopic phenomena and underlies modern technology. The particle-in-a-box model demonstrates energy quantization due to boundary conditions, yielding \( E_n = \frac{n^2 h^2}{8mL^2} \). The quantum harmonic oscillator, with energy levels \( E_n = \hbar\omega(n + 1/2) \), illustrates zero-point energy. The Mach–Zehnder interferometer models superposition and interference using two-state systems in \( \mathbb{C}^2 \), showing how measurement destroys interference.

### Relation to Other Theories

Classical mechanics emerges as an approximation via the correspondence principle, where quantum predictions reduce to classical ones at large scales. Quantization maps classical models to quantum ones. Quantum field theory (QFT) extends quantum mechanics to relativistic regimes, unifying quantum mechanics with special relativity. Quantum electrodynamics (QED) describes electromagnetic interactions with extraordinary precision. The Standard Model incorporates quantum chromodynamics (QCD) for the strong force and electroweak theory unifying electromagnetic and weak forces.

General relativity and quantum mechanics remain incompatible, motivating searches for quantum gravity. String theory replaces particles with vibrating strings, predicting gravitons. Loop quantum gravity models spacetime as spin networks evolving into spin foams at the Planck scale (\( \sim 1.616 \times 10^{-35} \) m).

### Philosophical Implications

Interpretations abound due to quantum mechanics' counter-intuitive nature. The Copenhagen interpretation treats probabilities as fundamental, rejecting classical causality. Einstein favored deterministic hidden variables, leading to the EPR paradox. Bell's theorem showed local hidden variables conflict with quantum predictions, confirmed by experiments violating Bell inequalities. Bohmian mechanics restores determinism via nonlocal guiding equations. Everett's many-worlds interpretation posits all outcomes occur in parallel universes. Relational quantum mechanics and QBism offer modern perspectives on measurement and observer roles.

## Terms

- **Hilbert space**: A complete inner product space where quantum states are represented as vectors.
- **Observable**: A Hermitian operator corresponding to a measurable physical quantity.
- **Eigenstate**: A quantum state that yields a definite value (eigenvalue) for an observable upon measurement.
- **Superposition**: A quantum state being a linear combination of multiple eigenstates simultaneously.
- **Born rule**: The rule assigning probabilities to measurement outcomes via the squared modulus of probability amplitudes.
- **Wave function collapse**: The postulate that measurement reduces a quantum state to an eigenstate of the measured observable.
- **Schrödinger equation**: The differential equation governing deterministic time evolution of quantum states.
- **Uncertainty principle**: The fundamental limit on simultaneous precision of conjugate observables.
- **Entanglement**: Quantum correlation where composite system states cannot be factored into individual subsystem states.
- **Bell's theorem**: The result showing local hidden variable theories cannot reproduce quantum mechanical predictions.

## Debates and Open Questions

The interpretation of quantum mechanics remains unresolved. Debates center on wave function collapse, the measurement problem, and quantum nonlocality. Einstein's quest for a deterministic theory led to hidden variable proposals, but Bell's theorem and experimental violations of Bell inequalities have constrained such approaches. Bohmian mechanics and many-worlds offer deterministic alternatives, yet face challenges in deriving the Born rule and explaining perceived probabilities. The reconciliation of quantum mechanics with general relativity—quantum gravity—remains an open frontier, with string theory and loop quantum gravity as leading candidates. Whether quantum effects can manifest macroscopically (beyond superconductors and superfluids) and the role of decoherence in classical emergence are active areas of research.

Source: adapted from "Quantum mechanics" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Quantum_mechanics

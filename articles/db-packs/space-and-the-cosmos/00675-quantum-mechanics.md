# Quantum mechanics

Quantum mechanics is the physical theory that describes matter and light at atomic and subatomic scales, where classical physics fails. Its central idea is that systems are described by *wave functions*, mathematical objects from which only probabilities for measurement outcomes can be predicted. The probabilistic core is a feature of nature: a deterministic law governs how the wave function changes over time, yet a single measurement yields a single, unpredictable result.

## The mathematical framework

The state of a quantum system is a normalized vector $\psi$ in a complex Hilbert space $\mathcal{H}$—a vector space with an inner product that lets lengths and angles be defined. States are fixed only up to an overall phase factor $e^{i\alpha}$, which has no physical effect. *Observables*, the measurable quantities such as position, momentum, and energy, are represented by Hermitian linear operators on this space (Hermitian meaning their eigenvalues, the possible measurement values, are real). A state may be an *eigenstate* of an observable, giving that observable's value with certainty, or a *superposition* of several eigenstates at once.

The **Born rule** turns the wave function into probabilities: the chance of measuring a value $a$ is $|\langle a|\psi\rangle|^2$. Upon measurement, the wave function *collapses* onto the corresponding eigenstate. Between measurements, time evolution is deterministic and follows the **Schrödinger equation**:

$$i\hbar \frac{\partial}{\partial t} \psi(t) = H \psi(t),$$

where $H$ is the Hamiltonian operator encoding the system's total energy. The formal solution is $\psi(t) = e^{-iHt/\hbar}\,\psi(0)$; the exponential factor is *unitary*, meaning it preserves total probability.

## Key phenomena

The **uncertainty principle** follows because conjugate observables do not commute. For position $\hat{X}$ and momentum $\hat{P}$, the relation $[\hat{X}, \hat{P}] = i\hbar$ forces $\sigma_X \sigma_P \geq \hbar/2$: the more precisely one is known, the less precisely the other can be. Geometrically, position and momentum wave functions are Fourier transforms of each other (each encodes the other as a sum of waves of different wavelengths), so narrowing one necessarily broadens the other.

In the **double-slit experiment**, particles sent one at a time through two slits build up an interference pattern when unobserved, but behave as classical particles when a which-path measurement is made. This wave–particle duality, proposed by de Broglie in 1923, shows that quantum objects are neither waves nor particles in the classical sense.

**Quantum tunneling** lets a particle cross a potential barrier that classical physics forbids. It enables radioactive alpha decay and scanning tunneling microscopy, where electrons tunnel across a vacuum gap between a sharp tip and a surface to image individual atoms.

**Entanglement** occurs when a composite system's state cannot be factored into independent states for each part; the joint space is the tensor product $\mathcal{H}_{AB} = \mathcal{H}_A \otimes \mathcal{H}_B$. Measuring one particle of an entangled pair fixes its correlation with the partner, yet this cannot transmit information faster than light. Entanglement is the resource behind quantum computing and quantum key distribution.

## Applications

Even simple textbook models capture the quantization seen in real atoms. A particle in a one-dimensional box of length $L$ has energies $E_n = n^2 h^2 / (8mL^2)$. A quantum harmonic oscillator has levels $E_n = \hbar\omega(n + \tfrac{1}{2})$, including a nonzero ground-state energy called zero-point energy. The Mach–Zehnder interferometer models two-state superpositions in $\mathbb{C}^2$ and shows how a which-path measurement destroys interference. The same quantization principles underpin lasers and semiconductor electronics.

## Historical development

The theory was assembled rapidly: Planck quantized energy in 1900; Einstein used light quanta in 1905; Bohr modeled the hydrogen atom with quantized orbits in 1913; de Broglie proposed matter waves in 1923; Heisenberg, Born, and Jordan built matrix mechanics and Schrödinger wave mechanics in 1925; Born introduced the probabilistic interpretation in 1926; Einstein, Podolsky, and Rosen published the EPR paradox in 1935; and Bell proved in 1964 that no local hidden-variable theory can reproduce quantum predictions, later confirmed by experiment.

## Relation to other theories

Classical mechanics emerges through the **correspondence principle**: at large quantum numbers or macroscopic scales, quantum predictions approach classical ones. Quantum field theory extends the formalism to relativistic regimes, with quantum electrodynamics (QED) describing electromagnetism to extraordinary precision and the Standard Model incorporating quantum chromodynamics (QCD) and electroweak theory. General relativity and quantum mechanics remain mutually incompatible. String theory replaces point particles with vibrating strings and predicts a graviton; loop quantum gravity models spacetime as spin networks evolving into spin foams at the Planck scale ($\sim 1.616 \times 10^{-35}$ m).

## Interpretations and open questions

Because measurement outcomes are random but evolution is deterministic, the meaning of the wave function is debated. The Copenhagen interpretation treats probabilities as fundamental. Einstein favored deterministic hidden variables, but Bell's theorem showed that any *local* hidden-variable theory conflicts with quantum predictions, a result now confirmed experimentally. Bohmian mechanics restores determinism using nonlocal guiding equations, while Everett's many-worlds interpretation holds that all outcomes occur in branching parallel universes. Modern perspectives include relational quantum mechanics and QBism. Reconciling quantum mechanics with general relativity to produce a working theory of quantum gravity remains an open frontier.

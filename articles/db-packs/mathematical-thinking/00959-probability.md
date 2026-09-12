# Probability

Probability quantifies how likely an event is, expressed as a number between 0 (impossible) and 1 (certain). It supplies a mathematical framework, probability theory, for modeling uncertainty, reasoning from data, and describing complex systems. The modern theory, formalized by Andrey Kolmogorov in 1931, treats probability as a *measure* (a rule that assigns sizes to sets) on a *sample space*, the set of all possible outcomes, and requires that measure to satisfy specific axioms.

Two interpretive traditions shape how the numbers are read. **Frequentists** (objectivists) identify probability with the long-run relative frequency of an outcome across repeated trials. **Bayesians** (subjectivists) treat probability as a degree of belief, starting from a *prior* distribution (what was believed before seeing data) and updating it with evidence to obtain a *posterior* distribution, via Bayes' theorem. The two camps disagree about what a probability fundamentally *is*, but the mathematics they use is largely the same.

## Core Mechanics

An **experiment** produces outcomes; the **sample space** Ω lists every possible one. A subset of Ω is an **event**, such as {1, 3, 5} for rolling an odd number on a die. A probability function assigns each event a value in [0, 1], with P(Ω) = 1, and obeys *countable additivity*: for mutually exclusive events, the probability of their union is the sum of their individual probabilities.

The basic rules follow from that definition:

- **Complement**: P(not A) = 1 − P(A).
- **Joint probability**: P(A ∩ B) is the probability both occur.
- **Independent events**: P(A ∩ B) = P(A) P(B), so two heads in two coin flips = 1/2 × 1/2 = 1/4.
- **Mutually exclusive events**: P(A ∩ B) = 0, and P(A ∪ B) = P(A) + P(B).
- **General addition rule**: P(A ∪ B) = P(A) + P(B) − P(A ∩ B), correcting the double-counting of overlap.
- **Conditional probability**: P(A|B) = P(A ∩ B) / P(B), the probability of A given that B occurred. Bayes' rule inverts this: posterior ∝ prior × likelihood, so P(A|B) ∝ P(A) P(B|A).

A **Markov chain** extends these ideas to sequences: a *stochastic process* in which the next state depends only on the current one, not the path taken to reach it. The **normal distribution**, the symmetric bell-shaped curve derived independently by Laplace, Adrain, and Gauss, is the continuous distribution that describes measurement error and many natural phenomena; the **method of least squares**, introduced by Legendre in 1805, fits curves to data by minimizing squared deviations.

## Origins

The field grew from gambling puzzles rather than abstraction. Cardano (16th century) framed odds as the ratio of favorable to unfavorable outcomes. In 1654, Fermat and Pascal corresponded on gambling problems and effectively founded the doctrine of probabilities. Huygens (1657), Bernoulli's posthumous *Ars Conjectandi* (1713), and de Moivre's *Doctrine of Chances* (1718) turned it into a recognized branch of mathematics. The **theory of errors** arose in parallel for observational data, with Laplace's first law of error (1774) and second law of error (1778) — the second being the normal distribution. Markov (1906) introduced Markov chains, and Kolmogorov (1931) gave probability its measure-theoretic foundation.

## Applications

Probability underpins risk modeling in insurance, finance, and regulation; reliability engineering for consumer products; biology, where it describes disease spread and genetics; and natural language processing, whose statistical language models are built on probability theory. Casinos design games using probability to guarantee long-run profit while keeping individual outcomes engaging.

## Probability and Physical Reality

Whether probability is fundamental or merely a stand-in for ignorance remains contested. In a deterministic Newtonian universe, Laplace's demon, an imaginary intellect that, knowing every particle's position and momentum, would predict the future exactly, shows that probability would be unnecessary if every initial condition were known. In practice, sensitivity to initial conditions and the impossibility of tracking ~10²³ molecules in a gas force statistical descriptions.

Quantum mechanics makes the question sharper. The wave function, a mathematical object whose squared magnitude gives the probability of finding a particle at each location, evolves deterministically, but under the Copenhagen interpretation, observation collapses it into a probabilistic outcome. Einstein ("God does not play dice") and Schrödinger rejected this indeterminism, hoping quantum mechanics was a statistical approximation of a hidden deterministic reality. Modern work on **quantum decoherence**, the loss of quantum coherence as a system interacts with its environment, explains the appearance of probabilistic outcomes even from underlying unitary physics. Other axiomatizations of uncertainty, including Dempster–Shafer theory and possibility theory, exist for special purposes but are incompatible with standard probability laws.

Persistent disagreements include the frequentist–Bayesian split (Bayesian agents with similar priors converge, but very different priors can sustain disagreement), whether quantum probability is ontologically real or epistemic, and the *reference class problem*: defining the "experiment" and its "outcomes" in real applications, where probabilities are rarely assessed independently or rationally.

# Probability

## Overview
Probability is the mathematical study of how likely events are to occur, quantified as a number between 0 (impossible) and 1 (certain). It provides an axiomatic framework—probability theory—used across statistics, science, finance, artificial intelligence, and philosophy to model uncertainty, draw inferences from data, and describe complex systems. The field bridges two major interpretive traditions: **objectivist** views (e.g., frequentist probability, which defines probability as the long-run relative frequency of outcomes) and **subjectivist** views (e.g., Bayesian probability, which treats probability as a degree of belief updated via evidence). Modern probability theory, formalized by Andrey Kolmogorov in 1931 using measure theory, defines probability as a measure on a sample space (the set of all possible outcomes) satisfying specific axioms.

## Timeline
- **16th century** — Gerolamo Cardano defines odds as the ratio of favorable to unfavorable outcomes.
- **1654** — Pierre de Fermat and Blaise Pascal correspond on gambling problems, founding the doctrine of probabilities.
- **1657** — Christiaan Huygens publishes the earliest scientific treatment of probability.
- **1713** — Jakob Bernoulli's *Ars Conjectandi* (posthumous) treats probability as a branch of mathematics.
- **1718** — Abraham de Moivre publishes *The Doctrine of Chances*.
- **1774** — Pierre-Simon Laplace publishes the first law of error (exponential function of error magnitude).
- **1778** — Laplace proposes the second law of error (exponential function of the square of the error), later known as the normal distribution.
- **1805** — Adrien-Marie Legendre develops the method of least squares.
- **1808** — Robert Adrain deduces the law of facility of error (normal distribution) independently.
- **1906** — Andrey Markov introduces Markov chains, advancing stochastic processes.
- **1931** — Andrey Kolmogorov formalizes modern probability theory based on measure theory.

## Body

### Etymology and Interpretations
The word *probability* derives from the Latin *probabilitas*, originally meaning "probity"—a measure of a witness's authority in legal contexts, often tied to nobility. This contrasts with the modern meaning: a measure of the weight of empirical evidence derived from inductive reasoning. In theoretical settings, **theoretical probability** is calculated as desired outcomes divided by total possible outcomes (e.g., 1/4 for two heads in two coin tosses). **Empirical probability** deals with observed frequencies in real experiments. Two major interpretive camps exist: **Objectivists** (frequentists) view probability as the objective, long-run relative frequency of an outcome in repeated trials; **propensity probability** modifies this to a physical tendency for a single trial. **Subjectivists** (Bayesians) view probability as a degree of belief, updated by combining a **prior probability distribution** (expert knowledge) with a **likelihood function** (data) to yield a **posterior probability distribution** via Bayes' theorem.

### Historical Development
Mathematical probability emerged slowly despite ancient gambling interests, hindered by superstition and the pre-17th-century meaning of "probable" as merely "approvable." Cardano (16th century) established the ratio of favorable to total outcomes. The formal doctrine began with the Fermat-Pascal correspondence (1654) on gambling problems. Huygens (1657), Bernoulli (1713), and de Moivre (1718) established it as a mathematical branch. The **theory of errors** developed in parallel: Roger Cotes (1722), Thomas Simpson (1755/56), and Laplace (1774, 1778) formulated laws of error, the second being the **normal distribution** (Gauss law). Legendre (1805) introduced the **method of least squares**; Adrain (1808) and Gauss (1809) independently derived the normal distribution. Nineteenth-century contributors included Laplace, Quetelet, De Morgan, and Boole. Markov (1906) introduced **Markov chains** for stochastic processes. Kolmogorov (1931) provided the modern measure-theoretic foundation.

### Mathematical Theory and Formalization
Probability theory represents concepts in formal terms manipulated by mathematics and logic. Two successful axiomatizations exist: **Kolmogorov's formulation** interprets sets as events and probability as a measure on a class of sets (a probability space); **Cox's theorem** takes probability as a primitive and focuses on consistent assignment of values to propositions. Both yield the same laws. Other uncertainty frameworks (Dempster–Shafer theory, possibility theory) exist but are incompatible with standard probability laws.

### Core Mathematical Treatment
An **experiment** yields results; the **sample space** (Ω) is the set of all possible results. The **power set** of Ω contains all subsets, called **events** (e.g., rolling an odd number on a die is the event {1,3,5}). A probability function assigns every event a value in [0,1], with P(Ω)=1, and requires **countable additivity**: for mutually exclusive events, the probability of their union equals the sum of their probabilities.
*   **Complement**: P(not A) = 1 − P(A).
*   **Intersection (Joint Probability)**: P(A ∩ B) is the probability both A and B occur.
*   **Independent Events**: P(A ∩ B) = P(A)P(B) (e.g., two heads in two coin flips = 1/2 × 1/2 = 1/4).
*   **Mutually Exclusive Events**: P(A ∩ B) = 0; P(A ∪ B) = P(A) + P(B).
*   **General Addition Rule**: P(A ∪ B) = P(A) + P(B) − P(A ∩ B) (corrects for double-counting overlap).
*   **Conditional Probability**: P(A|B) = P(A ∩ B) / P(B), the probability of A given B occurred (undefined if P(B)=0 unless using σ-algebras).
*   **Bayes' Rule (Inverse Probability)**: Posterior ∝ Prior × Likelihood; P(A|B) ∝ P(A)P(B|A). It updates beliefs (priors) with evidence (likelihood) to form posteriors.

### Applications
Probability underpins **risk assessment** and modeling in insurance (actuarial science), finance (equity trading, behavioral finance), government regulation, and biology (disease spread, genetics). In **reliability engineering**, it reduces failure probability in consumer products (automobiles, electronics), influencing warranty decisions. **Casinos** design games using probability to guarantee profit while maintaining player engagement. **Natural language processing** (e.g., cache language models) relies on statistical language models derived from probability theory.

### Relation to Randomness and Quantum Mechanics
In a **deterministic** Newtonian universe (Laplace's demon), probability would be unnecessary if all initial conditions were known perfectly. However, practical limits (sensitivity to initial conditions, complexity of systems like kinetic gas theory with ~10²³ molecules) make statistical descriptions necessary. **Quantum mechanics** fundamentally requires probability: the wave function evolves deterministically, but the **Copenhagen interpretation** holds that observation collapses the wave function, yielding probabilistic outcomes. This indeterminism was famously rejected by Einstein ("God does not play dice") and Schrödinger, who viewed quantum mechanics as a statistical approximation of a hidden deterministic reality. Modern interpretations invoke **quantum decoherence** to explain the appearance of probabilistic outcomes.

## Terms
- ****Sample Space (Ω)**** — The set of all possible outcomes of an experiment.
- ****Event**** — A subset of the sample space; a collection of outcomes to which a probability is assigned.
- ****Probability Measure**** — A function assigning a value in [0,1] to events, satisfying P(Ω)=1 and countable additivity for disjoint events.
- ****Independent Events**** — Events A and B where the occurrence of one does not affect the probability of the other; P(A ∩ B) = P(A)P(B).
- ****Mutually Exclusive Events**** — Events that cannot occur simultaneously; P(A ∩ B) = 0.
- ****Conditional Probability P(A\** — B)** The probability of event A given that event B has occurred; defined as P(A ∩ B)/P(B).
- ****Prior Probability**** — In Bayesian inference, the probability distribution representing belief before observing new data.
- ****Posterior Probability**** — The updated probability distribution after incorporating new evidence via Bayes' theorem.
- ****Normal Distribution**** — The "second law of error" (Laplace/Gauss); a continuous probability distribution symmetric about the mean, describing many natural phenomena.
- ****Markov Chain**** — A stochastic process where the probability of future states depends only on the current state, not the sequence of past states.

## Debates and open questions
*   **Frequentist vs. Bayesian Interpretation**: Whether probability represents an objective long-run frequency (frequentist) or a subjective degree of belief updated by evidence (Bayesian). The source notes Bayesian agents with similar priors converge (Aumann's agreement theorem), but sufficiently different priors can lead to persistent disagreement.
*   **Determinism vs. Indeterminism in Physics**: Whether quantum probability reflects fundamental ontological randomness (Copenhagen interpretation) or epistemic ignorance of hidden variables (Einstein, Schrödinger, modern decoherence approaches).
*   **Reference Class Problem**: Implicit in the definition of probability as a measure on a sample space; the source notes the difficulty of defining the "experiment" and "outcomes" in practical applications (e.g., "probabilities are neither assessed independently nor necessarily rationally" in financial markets).
# Markov logic network

A Markov logic network (MLN) is a probabilistic logic that applies Markov networks to first-order logic, defining a probability distribution over the possible worlds of a finite domain. Where first-order logic asks whether a world strictly satisfies a set of rules, an MLN softens them: worlds that satisfy more rules, especially rules with large positive weights, are more probable.

## Syntax

An MLN is a set of first-order formulas, each given a real-valued weight. A positive weight makes the formula a preference for being true; a negative weight makes it a preference for being false. A small example:

- 2.0 :: smokes(X) ← smokes(Y) ∧ influences(X,Y)
- 0.5 :: smokes(X) ← stress(X)

The first rule carries a larger weight because the friendship pattern is stronger than the stress effect.

## Semantics

Given a finite domain of objects, each predicate symbol is expanded into one Boolean ground atom for every tuple of domain elements it can take. For a domain {Alice, Bob}, smokes becomes smokes(Alice) and smokes(Bob), while influences becomes influences(Alice, Bob), influences(Bob, Alice), and so on. An interpretation assigns true or false to every ground atom. A grounding of a formula with free variables x₁,…,xₙ is the result of substituting specific domain elements; it is true in an interpretation when the substituted formula evaluates to true.

The probability of any interpretation is

P ∝ exp(Σⱼ wⱼ nⱼ)

where wⱼ is the weight of the j-th formula and nⱼ is the number of its true groundings. An interpretation that satisfies many high-weight formulas is exponentially more probable than one that violates them.

Equivalently, an MLN induces a Markov network whose nodes are the ground atoms and whose features are the ground formulas: each true ground formula contributes a factor of eʷ, and each false grounding contributes 1.

## Inference

The distribution an MLN defines can be queried for the probability of an atomic formula, called marginal inference, or for that probability conditioned on another atomic formula. Marginal inference is done with standard Markov network methods, restricted to the minimal subgraph of ground atoms needed for the query. Exact inference is #P-complete in the domain size, so probabilities are usually approximated. Common approximations are Gibbs sampling, belief propagation, and pseudolikelihood. When every formula uses at most two variables, exact inference is tractable by reduction to weighted model counting.

## Origin and use

Relational Markov networks, the immediate precursor, were introduced in 2002 by Ben Taskar, Pieter Abbeel, and Daphne Koller as domain-independent templates for Markov networks. Work on Markov logic networks itself began in 2003 with Pedro Domingos and Matt Richardson. MLNs are a common formalism in statistical relational learning, alongside Markov random fields, probabilistic logic networks, probabilistic soft logic, and ProbLog. The trade-off is expressive power against computational cost: a handful of weighted rules can encode rich relational dependencies, but answering probabilistic queries against them is generally intractable and must usually be approximated.

Source: adapted from "Markov logic network" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Markov_logic_network

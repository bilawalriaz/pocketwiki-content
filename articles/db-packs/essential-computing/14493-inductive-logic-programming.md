# Inductive logic programming

Inductive logic programming (ILP) is a subfield of symbolic AI that learns logical rules from data. Given background knowledge, positive examples, and negative examples, an ILP system produces a hypothesised logic program (a set of logical clauses) that explains the positives and excludes the negatives. The "inductive" here means philosophical induction — proposing a theory to explain observed facts — rather than mathematical induction. Bioinformatics and drug design have been the principal application areas.

## The basic schema

Every ILP task follows the same shape:

> **positive examples** + **negative examples** + **background knowledge** ⇒ **hypothesis**

A clause is an if-then rule of the form `head ← body`, where the body is a conjunction of conditions. A *ground* literal has no variables; a *substitution* replaces variables with specific terms.

## Two learning settings

In **learning from entailment**, the most common setting, examples are finite sets of ground literals. A correct hypothesis must satisfy two conditions:

- **Completeness**: background knowledge plus hypothesis entails all positive examples.
- **Consistency**: background knowledge, hypothesis, and negative examples do not entail a contradiction.

In **learning from interpretations**, examples are complete or partial Herbrand structures (mini-worlds described by ground facts). Correctness means every positive example is a model of the hypothesis combined with the background, and no negative example is.

## A short history

Gordon Plotkin first formalised induction in a clausal setting around 1970 by generalising from examples. In 1981, Ehud Shapiro built the Model Inference System, a Prolog program that learned Horn-clause programs from positive and negative examples. Stephen Muggleton coined the term "Inductive Logic Programming" in 1990, defined as the intersection of machine learning and logic programming.

Three influential 1990s systems shaped the field:

| System | Year | Approach |
|---|---|---|
| FOIL | 1990 | Extended propositional learners to first-order logic |
| Golem | 1990 | Used Plotkin's least generalisation |
| Progol | 1995 | Introduced inverse entailment |

Aleph (2001), a Progol descendant, remained widely used. By 2000, ILP had been applied to mutagenicity and carcinogenicity prediction and to protein structure and function, shifting the field toward relational data mining. The 2014 Metagol system revived harder tasks — predicate invention and recursive programs — through meta-interpretive learning, which lets ILP work with far fewer examples.

## How systems search for a hypothesis

The space of all possible clauses forms a *lattice* under *subsumption*: one clause subsumes another when a substitution makes it a subset. Search-based systems traverse this lattice either bottom-up or top-down.

**Bottom-up methods** build hypotheses by generalising from examples toward broader rules. The least general generalisation of two clauses is the most specific clause that subsumes both, found by anti-unification, matching literals that share a predicate. *Relative* least general generalisations incorporate background knowledge and underpin Golem. *Inverse resolution*, introduced by Muggleton and Buntine in 1988 in the Cigol system, inverts the resolution inference rule: given a resolvent and one parent clause, it guesses the missing parent. V-operators reconstruct one parent from a resolvent and a sibling; W-operators reconstruct an entire chain.

**Top-down methods** use inverse entailment: given that background knowledge and hypothesis should entail the examples, they derive what the hypothesis must look like. Progol, Hail, and Imparo build an intermediate bridge theory and generalise it. Progol's search is not complete in general (Yamamoto's 1997 example shows it can miss hypotheses), while Imparo achieves completeness through inverse subsumption, a less non-deterministic variant.

**Meta-interpretive learning** replaces explicit search with a meta-level logic program that the system solves to produce a hypothesis. Metagol uses a Prolog meta-interpreter; ILASP and ASPAL encode the problem in answer set programming. This style handles predicate invention and recursion more easily.

## Probabilistic ILP

Standard ILP produces rules that either hold or do not. Probabilistic inductive logic programming extends the setting to probabilistic logic programs, where each clause carries a probability and the goal is to maximise the probability of positive examples while minimising that of negatives. The task splits into parameter learning (fix the rule structure, learn probabilities, typically by expectation-maximisation or gradient descent) and structure learning (discover both the rules and the probabilities). Structure learning was pioneered by Daphne Koller and Avi Pfeffer in 1997; later systems include ProbFOIL (2010), SLIPCASE (2011), and SLIPCOVER (2014), which combine beam search over clauses with greedy search over theories. Probabilistic ILP is a branch of statistical relational learning, where uncertainty meets relational structure.

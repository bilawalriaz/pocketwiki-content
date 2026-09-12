# Algorithmic probability

Algorithmic probability, also called Solomonoff probability, assigns a prior probability to any observation by treating it as the output of a computer program. Ray Solomonoff introduced it in the 1960s as the basis of a general theory of inductive inference. Given a sequence of symbols, the theory asks which symbol comes next and answers by combining a prior over programs with Bayes' rule.

## The core idea

An observation is a finite binary string. A reference computer, which may be any universal Turing machine, is fed random programs and the strings those programs print. Each program is weighted by its length, with shorter programs receiving more probability mass. The algorithmic probability of a string is the total weight of all programs that begin by printing it. Shorter programs are exponentially more probable, so a string with any short program that generates it has high probability, while a string generated only by a long program has low probability. No string has zero probability, since every string has at least one valid program, and the distribution is universal in the Turing-computability sense.

The construction encodes two informal principles. Occam's razor, "choose the simplest theory consistent with the observations," is the inverse weighting by program length. Epicurus' principle of multiple explanations, "keep every theory consistent with the observations," is the sum over all such programs rather than a choice among them.

## A semi-measure, not a true probability

The algorithmic probability P(x) is not a true probability distribution but a semi-measure, so the sum of P(x) over all strings is strictly less than one. The missing mass comes from programs that never halt: the probability placed on them is lost. P is not computable. It is only lower semi-computable, since a Turing machine can print an increasing sequence converging to P(x) from below, but no machine can converge from above.

## Relation to Kolmogorov complexity

Algorithmic probability is the probabilistic twin of Kolmogorov complexity. The Kolmogorov complexity K(x) of a string x is the length of the shortest program that prints x on a universal Turing machine. Solomonoff's universal distribution assigns a string x the sum of 2 to the power minus the length of each program that generates it, restricted to prefix-free programs so that no program is a prefix of another, which gives the required independence among causes. The prefix-free condition lets Kraft's inequality bound the sum by one.

The invariance theorem states that switching between any two Turing-complete reference machines changes Kolmogorov complexity by only a constant, since a compiler from one language to the other is a finite program whose length fixes the constant. Solomonoff proved that algorithmic probability is invariant in the same machine-independent sense up to a constant factor.

## Limits on computability

The universal distribution is the optimal prior among computable hypotheses, but at a heavy cost. Evaluating it exactly requires running every program that could produce the observation, including those that never halt, so the computation can be infinite. Levin's universal search mitigates this by allotting more time to shorter programs, producing a sequence of approximations that converge to the true distribution as more time is allowed. Other approximations restrict the search space with training sequences.

## Hutter's AIXI

Marcus Hutter extended Solomonoff's framework to sequential decisions as AIXI, an agent that picks actions to maximise expected reward summed over futures, weighted by their algorithmic probabilities. AIXI is optimal among all agents in any computable environment, but is itself incomputable and needs exponential time in the worst case. Time-bounded variants such as AIXItl preserve most of its theoretical properties while remaining feasible. The framework assumes the environment is computable, so genuinely chaotic or non-computable systems fall outside its scope, and the modelling of non-computable universes remains an open question.

Source: adapted from "Algorithmic probability" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Algorithmic_probability

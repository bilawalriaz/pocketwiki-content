# Evolvability (computer science)

Evolvability is a framework of computational learning introduced by Leslie Valiant in his 2006 paper of the same name. It models biological evolution mathematically and classifies which function classes can be reached by gradual local search. The framework extends PAC learning (probably approximately correct learning, in which a learner picks a hypothesis from arbitrary examples) and learning from statistical queries.

## The general framework

Two function classes act on $n$ variables: an ideal function class $F_n$ (the target phenotype) and a representation class $R_n$ (the genotype that evolution actually searches). Given a hidden ideal $f \in F_n$, the goal is to find, by small local steps, a representation $r \in R_n$ that closely approximates $f$.

Genotype and phenotype can diverge: distinct representations $r, r' \in R_n$ may compute the identical function on every input. The search only changes the genotype a little at a time. The neighbourhood $N(r)$ is the set of all one-step mutations of $r$.

For concreteness, take Boolean functions on $X_n = \{-1, 1\}^n$ and let $D_n$ be a probability distribution on $X_n$. The performance of $r$ against $f$ is

$$\operatorname{Perf}(f, r) = \sum_{x \in X_n} f(x)\, r(x)\, D_n(x).$$

In the Boolean case this equals $\operatorname{Prob}(f(x) = r(x)) - \operatorname{Prob}(f(x) \neq r(x))$, ranging from $-1$ (perfect mismatch) to $+1$ (perfect match). For non-Boolean functions the formula still measures agreement but loses the probability-of-agreement interpretation.

An organism never sees the whole distribution, so define empirical performance on a sample $S$ of $s$ independent draws from $D_n$:

$$\operatorname{Perf}_s(f, r) = \frac{1}{s} \sum_{x \in S} f(x)\, r(x).$$

When $s$ is large, the empirical performance is close to the true performance.

## The mutator and one generation

Given $f$, current $r$, sample size $s$, and tolerance $t$, the mutator $\operatorname{Mut}(f, r, s, t)$ classifies every $r' \in N(r)$ by the change in empirical performance:

- **Beneficial** if $\operatorname{Perf}_s(f, r') - \operatorname{Perf}_s(f, r) \geq t$.
- **Neutral** if $-t < \operatorname{Perf}_s(f, r') - \operatorname{Perf}_s(f, r) < t$.
- **Deleterious** if $\operatorname{Perf}_s(f, r') - \operatorname{Perf}_s(f, r) \leq -t$.

If any beneficial mutation exists, the mutator returns one at random; otherwise it returns a random neutral mutation. Because $r$ itself counts as a mutation, the neutral set is never empty and the process cannot deadlock.

Evolution is iterating the mutator. Starting from $r_0$, define $r_{i+1} = \operatorname{Mut}(f, r_i, s, t)$, so after $g$ generations $r_g$ is the evolved representation.

## When is a class evolvable?

Three polynomial quantities control feasibility: the neighbourhood size $|N(r)| \leq p(n, 1/\epsilon)$, the sample size $s(n, 1/\epsilon)$, and the generation count $g(n, 1/\epsilon)$. The tolerance is $t(1/n, \epsilon)$.

A class $F$ is evolvable by $R$ over $D$ if, for every $n$ and every $\epsilon > 0$, every ideal $f \in F_n$ and every starting $r_0 \in R_n$ satisfy

$$\Pr\!\left[\operatorname{Perf}(f, r_{g(n, 1/\epsilon)}) \geq 1 - \epsilon\right] \geq 1 - \epsilon.$$

$F$ is evolvable over $D$ if some representation class $R$ makes it evolvable, and evolvable if it is evolvable over every distribution $D$.

## Known results

The class of conjunctions is evolvable over the uniform distribution; disjunctions are evolvable over the uniform distribution when restricted to short formulas. Parity functions (which output the parity of a chosen subset of literals) are not evolvable, even under the uniform distribution. Evolvability implies PAC learnability: every evolvable class is also PAC learnable.

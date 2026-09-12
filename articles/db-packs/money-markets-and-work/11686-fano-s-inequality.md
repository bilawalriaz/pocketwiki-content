# Fano's inequality

Fano's inequality, also called the Fano lemma or Fano converse, relates how much information a noisy channel destroys to how often a decoder gets the message wrong. Robert Fano derived it in the early 1950s while teaching a Ph.D. seminar at MIT, and it appeared in his 1961 textbook. The bound is used to lower-bound the error probability of any decoder and the minimax risk in density estimation. The term "converse" reflects its role as the opposite direction of Shannon's channel coding theorem: where Shannon shows reliable transmission is possible at low enough rates, Fano shows a minimum error is unavoidable at high enough rates.

## The setup

Let X be the discrete message sent and Y the message received, with joint probability P(x, y). A decoder is any function f producing an estimate X̃ = f(Y), and e denotes an error event, X̃ ≠ X. The inequality is:

**H(X | Y) ≤ H_b(e) + P(e) · log(|X| − 1)**

|X| is the number of possible messages, the cardinality of X. H(X | Y) is the conditional entropy, the remaining uncertainty about X after seeing Y, measured in bits. P(e) is the probability of error. H_b(e) is the binary entropy of the error indicator, equal to −P(e) log P(e) − (1 − P(e)) log(1 − P(e)), which is 0 when P(e) = 0 or P(e) = 1 and reaches 1 bit when P(e) = 1/2.

## Reading the bound

The left side is the uncertainty that survives even after observing Y. The right side has two ingredients. H_b(e) measures uncertainty about whether an error occurred; it is tiny when errors are rare and approaches 1 bit when they are common. P(e) · log(|X| − 1) scales the error probability by the log of the number of wrong alternatives. When an error happens, the decoder can rule out one value, so at most |X| − 1 possibilities remain.

Whenever the right side is large, Y must be leaking a lot of information about X. Equivalently, a small H(X | Y) forces P(e) to be small, which is why Fano's inequality is used to lower-bound error rates.

## Why it holds

The proof uses the Markov chain X → Y → X̃, meaning X̃ depends on X only through Y. The data processing inequality then gives H(X | X̃) ≥ H(X | Y), so it suffices to upper-bound H(X | X̃).

Define an indicator E that is 1 when X̃ ≠ X and 0 otherwise. The chain rule for entropies expands H(X | X̃) in two ways:

**H(X | X̃) = H(E | X̃) + H(X | E, X̃)**

When E = 0, knowing X̃ fixes X exactly, so H(X | E=0, X̃) = 0. When E = 1, the true value lies among |X| − 1 alternatives, so H(X | E=1, X̃) ≤ log(|X| − 1). Splitting on E gives H(X | E, X̃) ≤ P(e) · log(|X| − 1). Conditioning reduces entropy, so H(E | X̃) ≤ H(E) = H_b(e). Combining the bounds and replacing H(X | X̃) with the smaller H(X | Y) from the Markov chain yields the inequality.

## Intuition

The bound splits the receiver's residual uncertainty into two questions given a predictor: did it err, and if so, which of the remaining possibilities is right. A perfect predictor makes both terms vanish and forces H(X | Y) = 0, meaning Y determines X. If the predictor always errs, H_b(e) = 0 and H(X | Y) is bounded by log(|X| − 1), the entropy of a uniform distribution over the non-predicted values.

## Alternative formulation

Let X be drawn from one of r + 1 possible densities f₁, …, f_{r+1}, with every pair satisfying Kullback–Leibler divergence D_KL(f_i ‖ f_j) ≤ β. Kullback–Leibler divergence measures how distinguishable two distributions are in bits. For any estimator ψ(X) of which density generated the data, the worst-case error satisfies:

**sup_i P_i(ψ(X) ≠ i) ≥ 1 − (β + log 2) / log r**

When the candidate densities are hard to distinguish (small β) or there are many of them (large r), the bound approaches 1, forcing some pair to be confused almost surely.

## Generalisation to density estimation

Ibragimov and Khasminskii (1979) and Assouad and Birge (1983) extended the bound to density estimation. Given a class F of densities containing a sub-family of r + 1 members with L¹ separation at least α, meaning ∥f_θ − f_{θ'}∥_{L¹} ≥ α, and pairwise KL divergence at most β, any density estimator f_n built from n samples obeys:

**sup_{f ∈ F} E ∥f_n − f∥_{L¹} ≥ (α / 2) · (1 − (nβ + log 2) / log r)**

The L¹ norm sums absolute differences between densities. As n grows the right side shrinks, but it stays positive until n exceeds roughly (log r − log 2) / β. This gives a concrete sample-complexity lower bound: distinguishing many close densities requires at least that many samples.

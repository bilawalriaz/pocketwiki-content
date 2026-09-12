# Proof of knowledge

A proof of knowledge is an interactive protocol in which a prover convinces a verifier that the prover holds a secret value (a "witness"), not merely that some statement is true.

## What "knowing" means

A machine "knows" a value only if that value can be computed from the machine itself. A program that never outputs its secret may still be said to know it, provided another program, a **knowledge extractor**, can pull the secret out given access to the prover.

Concretely, fix a language $L$ in NP (the class of statements whose witnesses can be checked in polynomial time). Each statement $x \in L$ has a set of valid witnesses $W(x)$, captured by the witness relation
$$R = \{(x, w) : x \in L,\ w \in W(x)\}.$$

A proof of knowledge for $R$ is a two-party protocol between a prover $P$ and a verifier $V$ with two properties:

- **Completeness.** If $(x, w) \in R$, an honest prover holding $w$ convinces $V$ with probability 1:
$$\Pr\!\bigl[P(x,w) \leftrightarrow V(x) \rightarrow 1\bigr] = 1.$$
- **Validity.** There exists a polynomial-time knowledge extractor $E$ with oracle access to any (possibly malicious) prover $\tilde P$ such that $E$'s probability of producing a valid witness is at least the prover's probability of convincing $V$, minus a small **knowledge error** $\kappa(x)$:
$$\Pr\!\bigl[E^{\tilde P(x)}(x) \in W(x)\bigr] \geq \Pr\!\bigl[\tilde P(x) \leftrightarrow V(x) \rightarrow 1\bigr] - \kappa(x).$$
$E$ may output $\bot$ (no conclusion). A small $\kappa$ (e.g. $2^{-80}$ or $1/\mathrm{poly}(|x|)$) makes validity stronger than ordinary interactive-proof soundness.

## Why membership alone is not enough

In some languages, deciding membership is easy but producing the witness is hard. In a cyclic group $\langle g \rangle$ where the **discrete logarithm** problem (recovering $w$ from $g^w$) is hard, every $x$ in the group trivially satisfies $x \in \{x \mid g^w = x\}$, yet producing that $w$ is exactly the discrete-log problem. A useful proof must certify knowledge of a specific $w$, not just membership.

## The Schnorr protocol

The canonical proof of knowledge of a discrete log, due to Schnorr, runs in a cyclic group $G_q$ of order $q$ with generator $g$. To prove knowledge of $x = \log_g y$:

1. **Commitment.** $P$ picks random $r$ and sends $t = g^r$.
2. **Challenge.** $V$ sends a random $c$.
3. **Response.** $P$ sends $s = r + cx \pmod q$.

$V$ accepts iff $g^s = t\,y^c$.

The extractor rewinds $\tilde P$: from the same commitment $t$, it feeds two different challenges $c_1, c_2$ and gets $s_1 = r + c_1 x$, $s_2 = r + c_2 x$. Subtracting gives $s_1 - s_2 = x(c_1 - c_2)$, so the extractor recovers
$$x = (s_1 - s_2)(c_1 - c_2)^{-1}.$$
Anyone who answers two distinct challenges for one commitment must know $x$; conversely, knowing $x$ answers any challenge. The protocol is also zero-knowledge, though zero-knowledge is not required of proofs of knowledge in general.

## Sigma protocols

Any three-move protocol with the structure commitment–challenge–response is a **sigma protocol**, named for the zig-zag shape of its transcript combined with "MA" for Merlin-Arthur proofs. Sigma protocols compose: one can prove that two discrete logs satisfy a linear relation, not just that each exists. The notation
$$PK\{(x) : y_1 = g_1^{x} \wedge y_2 = (g_2^{a})^{x}\, g_2^{b}\}$$
states that the prover knows an $x$ linking $y_1, y_2$ through $x_2 = a x_1 + b$. The special case $a = 1, b = 0$ is a proof that two logarithms are equal.

## Applications

Proofs of knowledge underlie identification protocols, and their non-interactive variants yield signature schemes such as Schnorr signatures. They also underpin group signature and anonymous digital credential systems.

# Common knowledge (logic)

Common knowledge is a kind of group knowledge defined by infinite nesting of "knows that": everyone in a group *G* knows *p*, everyone knows that everyone knows *p*, everyone knows that everyone knows that everyone knows *p*, and so on without end. It is written as $C_G p$. By contrast, $E_G p$ means only that every agent in *G* knows *p* (first-order mutual knowledge); higher-order mutual knowledge is $E_G^n p$, the *n*-fold iteration. Common knowledge is the conjunction of every order: $C_G p$ holds when $E_G^n p$ holds for all finite *n*.

## Where the idea comes from

David Kellogg Lewis introduced the concept in philosophy in *Convention* (1969); sociologist Morris Friedell defined it independently the same year. Robert Aumann gave the first mathematical, set-theoretic formulation in 1976. Stephen Schiffer called the same idea "mutual knowledge" in 1972. Computer scientists working on epistemic logic took it up in the 1980s, and John Conway helped popularise it through puzzles.

## The blue-eyed islanders

The standard induction puzzle shows why the nesting matters. On an island, *k* people have blue eyes and the rest have green. Each person sees every other eye colour but not their own, and no one discusses it. An outsider publicly announces that at least one person has blue eyes, and the islanders already know the outsider is truthful.

Result: all *k* blue-eyed people leave on the *k*th dawn after the announcement.

The mechanism is induction on *k*. With *k = 1*, the lone blue-eyed person sees no other blue eyes, so the announcement must refer to them, and they leave at the first dawn. With *k = 2*, each blue-eyed person can see exactly one other; the announcement is informative because before it, neither can tell whether the count is one or two. When no one leaves on the first dawn, the two both infer the count is at least two and leave on the second. Each further dawn of inaction eliminates one possible count, so all *k* leave together on the *k*th dawn.

For *k > 1* the outsider is stating something every islander already knows: that at least one person has blue eyes. What the public announcement adds is the missing level of mutual knowledge. Before it, each blue-eyed islander has $(k-1)$-th order knowledge of the fact (they know of *k − 1* others who know, and so on, but the chain stops one level short). The announcement closes the chain, converting mutual knowledge into common knowledge, which is what lets the blue-eyed islanders deduce their own eye colour.

## Public versus private announcement

Common knowledge is fragile to the medium of communication. A trustworthy fact told to each agent in private, even if each is told that everyone was told, remains only mutual knowledge: $E_G E_G p \not\Rightarrow C_G p$, because each agent can be unsure that the others actually received the message. A single public announcement of a fact *p* makes *p* common knowledge, since everyone observes the same event and knows that everyone observes it: $C_G E_G p \Rightarrow C_G p$.

## Formal definition

In multi-modal epistemic logic, the "everyone knows" operator is $E_G \varphi \Leftrightarrow \bigwedge_{i \in G} K_i \varphi$, where $K_i \varphi$ means "agent *i* knows φ." Common knowledge is then the infinite conjunction $C_G \varphi \Leftrightarrow \bigwedge_{i=0}^{\infty} E_G^i \varphi$, equivalently the fixed point of $C_G \varphi = \varphi \wedge E_G(C_G \varphi)$. Because epistemic languages are finitary, the fixed-point form is the one used in proofs. Aumann's set-theoretic version says the same thing: an event *e* is common knowledge iff $C(e) = \bigcap_{n=1}^{\infty} E^n(e)$, where each $E^n$ is iterated mutual knowledge and the partitions for each agent are the basic units of uncertainty.

## Why it is used

In game theory, Aumann's agreement theorem shows that two agents with a common prior cannot "agree to disagree" once their posterior probabilities are common knowledge; the no-trade theorem extends this to show that speculative trade is impossible under the same conditions. On Lewis's account, a convention is behaviour sustained by common knowledge of expectations. In distributed computing, common knowledge cannot be established over a channel that may drop a message, which is why protocols like the Two Generals' Problem run into impossibility results when they try to guarantee agreement.

Source: adapted from "Common knowledge (logic)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Common_knowledge_%28logic%29

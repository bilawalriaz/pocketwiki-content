# Theory (mathematical logic)

In mathematical logic, a *theory* is a set of sentences in a formal language, usually paired with a deductive system that specifies how sentences follow from one another. Together, the language and the deduction rules form a *formal system*. A sentence $\phi$ belonging to a deductively closed theory $T$ (written $\phi \in T$) is a *theorem*. Most theories are generated from a small set of starting sentences called *axioms*, with the deductive system then called an *axiomatic system*; every axiom is automatically a theorem. A *first-order theory* is one whose sentences are first-order and whose theorems are produced recursively by applying inference rules to its axioms.

## Theories as subsets of statements

A theory is built by first fixing a non-empty conceptual class $\mathcal{E}$ whose elements are *statements*. The initial ones are *primitive* or *elementary* statements, distinguished from anything later derived. A theory $\mathcal{T}$ is then a conceptual class of some elementary statements, which are its *elementary theorems* and are declared true within $\mathcal{T}$. Under this view truth is relative to a theory: the same elementary statement can be true in one theory and false in another, just as "he is honest" requires a context to evaluate.

## Subtheories, extensions, and deductive closure

$\mathcal{S}$ is a *subtheory* of $\mathcal{T}$ when $\mathcal{S} \subseteq \mathcal{T}$, and an *extension* (or supertheory) when $\mathcal{T} \subseteq \mathcal{S}$. A theory is *deductive* when it rests on a formal deductive system and singles out some elementary statements as axioms; every logical consequence of its axioms is then also a sentence of the theory. Formally, if $\vdash$ is a Tarski-style consequence relation, $\mathcal{T}$ is closed under $\vdash$ exactly when $\mathcal{T} \vdash \phi$ implies $\phi \in \mathcal{T}$ for every sentence $\phi$ in its language.

## Consistency and completeness

A theory is *syntactically consistent* if not every sentence of its language is provable. In systems obeying the *principle of explosion* (everything follows from a contradiction), this is equivalent to: no sentence $\phi$ can be proved together with its negation. A theory is *satisfiable* if it has a *model*, a structure $M$ making every sentence true; every satisfiable theory is syntactically consistent, since a model satisfies exactly one of $\phi$ and its negation for each sentence. In first-order logic the *completeness theorem* makes the two notions coincide, but in stronger logics such as second-order logic, syntactically consistent but unsatisfiable theories, including $\omega$-inconsistent ones, exist.

A *complete* consistent theory $\mathcal{T}$ is one for which every sentence $\phi$ of its language is either provable from $\mathcal{T}$ or makes $\mathcal{T} \cup \{\phi\}$ inconsistent; for theories closed under consequence, $\mathcal{T}$ contains either $\phi$ or its negation for every $\phi$. A consistent theory that fails this is *incomplete*.

## Interpretations and the theories of a structure

An *interpretation* of a theory is a many-to-one correspondence between its elementary statements and statements about some subject matter; it is *full* if every elementary statement has a correspondent and *partial* otherwise. Every structure $A$ has an associated *complete theory* $\operatorname{Th}(A)$, the set of all first-order sentences in the signature of $A$ that $A$ satisfies. For a class $K$ of $\sigma$-structures, $\operatorname{Th}(K)$ is the set of first-order $\sigma$-sentences true in every member of $K$. An interpretation of a first-order theory supplies a semantics for its formulas; a *model* of the theory is an interpretation in which every formula is satisfied.

## Specifying a theory

The direct route is to write down a set of axioms; the theory is then those axioms together with their provable consequences. The second route starts from a structure and lets the theory be the set of sentences it satisfies, yielding complete theories semantically. The set of true sentences of $(\mathbb{N}, +, \times, 0, 1, =)$, called *true arithmetic*, is one such theory and cannot be captured as the logical consequences of any enumerable set of axioms. Tarski showed the analogous theory of $(\mathbb{R}, +, \times, 0, 1, =)$, the theory of real closed fields, to be decidable.

# Language identification in the limit

Language identification in the limit is a 1967 formal model, introduced by E. Mark Gold, for how a machine can infer a formal language from examples. A *formal language* here means any set of strings over some alphabet; examples include the set of all palindromes or all strings matching a given regular expression. A *presentation* is an infinite stream of strings that the language produces.

## The basic setup

Two roles interact over time:

- **Teacher** reveals a presentation of some unknown target language $L$.
- **Learner** reads each new string and outputs a *representation*, such as a regular expression or a grammar, as its current guess for $L$.

Learning is modelled as an infinite process. After each input the learner may revise its guess. The learner *identifies $L$ in the limit* if, after some finite stage, it stops changing its mind and settles on a correct representation forever. The learner never has to announce that it has converged, and the teacher can withhold the strings that would confirm the guess for as long as it likes.

Two presentation types matter:

- **Text (positive information):** the teacher enumerates all strings in $L$, each appearing at least once but in arbitrary order with repetitions.
- **Complete presentation:** the teacher enumerates all possible strings, labelling each as belonging to $L$ or not. Variants include "by telling" (teacher chooses order) and "by request" (learner picks which string to query).

## Identification in the limit

Formally, a *language* $L$ is a nonempty set of *sentences* (the sentences need only be distinguishable objects, not necessarily finite strings). A *language family* is a set of languages. A *language learner* is a function $f$ mapping a finite list of sentences seen so far to a guessed language. A learner *learns* $L$ in environment $E = (a_1, a_2, \ldots)$ if, after some finite number of inputs, it permanently outputs $L$. A learner *learns* $L$ if it does so in every environment for $L$. A family is *learnable* if some single learner learns every language in it.

Learnability is not a property of individual languages: any one language $L$ can be trivially learned by a learner that always guesses $L$. Learnability is a property of the family as a whole.

## Gold's theorem and its proof

Gold's 1967 theorem says: if a language family $C$ contains languages $L_1 \subsetneq L_2 \subsetneq \cdots$ with $L_\infty = \bigcup_n L_n$, then $C$ is not learnable.

The proof is a diagonal argument. Assume a learner $f$ can learn $L_1, L_2, \ldots$. Construct a single environment $E$ for $L_\infty$ that defeats $f$:

1. Feed $f$ an environment $E_1$ for $L_1$ until it outputs $L_1$.
2. Interleave the remaining data of $E_1$ with all of $E_2$. Because $L_1 \subset L_2$, the interleaving is still a valid environment for $L_2$, so $f$ must eventually switch to outputting $L_2$.
3. Continue by adding $E_3$, then $E_4$, and so on.

By construction, $E$ contains every $E_n$, so it contains $\bigcup_n L_n = L_\infty$, making it a valid environment for $L_\infty$. Yet $f$ keeps switching to $L_n$ for finite $n$ and never converges on $L_\infty$.

The theorem is easily bypassed with negative information. A learner can guess $L_\infty$ until it sees a string $a_n \in L_{n+1} \setminus L_n$ marked as not in $L_\infty$, after which it locks onto $L_n$. Each $L_n$ is then learned.

## Which families are learnable?

Dana Angluin (1980) gave the standard characterisations:

- For an *effective* (computable) learner, an indexed family of recursive languages is learnable from text iff there is a uniform procedure that, for each language, outputs a *tell-tale*: a finite set of strings that belongs to that language and to no other language in the family. This is Condition 1.
- For an *ideal* (possibly noncomputable) learner, the same characterisation holds but with "exists a tell-tale for each language" (Condition 2).

A useful sufficient condition is *finite thickness*: every nonempty set of strings is contained in only finitely many languages of the family. Finite thickness implies finite elasticity, which in turn implies the existence of a *mind change bound*: an a priori limit on how many times the learner may revise its guess before it must converge. Existence of a mind change bound implies learnability, though not conversely in the computable setting.

With normal text presentation (positive information only), only the finite languages and singletons are identifiable in the limit: regular, context-free, context-sensitive, and primitive recursive families are not. With complete presentation (positive and negative information), the boundary rises sharply: all regular languages, all context-free languages, and primitive recursive languages become identifiable. Adding anomalous text presentations pushes identifiability up to the recursively enumerable languages.

Pure positive information makes most interesting language families unlearnable, while adding negative information collapses the barrier.

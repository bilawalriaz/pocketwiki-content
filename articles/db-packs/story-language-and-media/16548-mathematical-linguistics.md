# Mathematical linguistics

Mathematical linguistics applies mathematics to model phenomena in general and theoretical linguistics, and overlaps heavily with computational linguistics. The field borrows tools from discrete mathematics, formal language theory, logic, signal processing, statistics, and graph theory, each tied to a specific sub-area of language study.

## Discrete mathematics

Set theory underlies the classification of linguistic objects: semantic classes, word classes, natural classes, and the allophonic variations of each phoneme in a language. Set operations and concatenation theory are standard tools in phonetics and phonology.

Combinatorics governs phonotactics, the rules that decide which sequences of phonemes a language permits. Counting over a fixed inventory of segments and constraints yields the total number of legal syllables or words; combinatorics on words also uncovers patterns inside morphemes and sentences.

Finite-state transducers (FSTs) implement context-sensitive rewriting rules of the form a → b / c _ d, the standard notation for phonological rules and sound change, provided application is non-recursive. Weighted FSTs power machine translation and other natural language processing tasks, and the OpenGrm library uses one for part-of-speech tagging.

## Algorithms, graphs, topology

Optimality theory (OT) and maximum-entropy phonotactics evaluate candidate phoneme strings against ranked constraints to determine a language's phonotactic grammar. Trees are the dominant graph structure in linguistics, used for parse trees, sentence diagrams, language-family trees, and etymological trees. Weighted graphs model lexical similarity between related languages, semantic networks encode meaning relations, and lattice graphs encode OT candidate evaluations.

Semantic topology applies circuit topology to discourse: by representing recurring themes as series, parallel, or cross configurations, analysts detect statistical differences in communication style across texts.

## Formal linguistics and logic

Formal linguistics analyses natural language with formal languages, formal grammars, and first-order logic; since the 1980s the label has usually meant Chomskyan linguistics. Generative frameworks such as head-driven phrase structure grammar have been re-deployed inside natural language processing.

Logic models syntax, formal semantics, and pragmatics. Modal logic captures grammatical mood, and most linguistic universals (including Greenberg's universals) are stated in propositional logic. Lexical relations between words can be defined by whether a word pair satisfies a conditional proposition:

| Lexical relation | Logical form | Example |
|---|---|---|
| Synonym | x ↔ y | pavement ↔ sidewalk |
| Complementary antonyms | (x → ¬y) ∧ (y → ¬x) | alive / dead |
| Gradable antonyms | (x → ¬y) ∧ (y → ¬x) | good / bad |
| Relational antonyms (nouns) | If A is B's X, then B is A's Y | parent / child |
| Relational antonyms (verbs) | If A Xs to B, then B Ys from A | give / receive |
| Relational antonyms (prepositions) | If A is X B, then B is Y A | below / above |
| Hyponym | X is a Y, but Y is not only an X | terrier → dog |
| Cohyponym | X and Y are both Zs | rose, tulip ⊂ flower |
| Meronym | the parts of a Y include the Xs | spoke ⊂ wheel |
| Quasi-meronym | an X belongs to a Y | tribesman ⊂ tribe |

## History and semiotics

Louis Hjelmslev, building on David Hilbert and Rudolf Carnap, proposed using formal grammars to analyse, generate, and explain language in his 1943 *Prolegomena to a Theory of Language*; Charles Sanders Peirce contributed earlier work. Their view treats language as a mathematical relation between meaning and form. J. R. Firth and Simon Dik extended formal description into frameworks such as systemic functional linguistics and functional discourse grammar. Lucien Tesnière's dependency grammar has been widely applied in natural language processing.

## Statistics

The fast Fourier transform, Kalman filters, and autoencoding are used in signal processing for advanced phonetics and speech recognition.

Statistical methods describe and validate research results, identify trends, and quantify corpus evidence. Student's t-test decides whether a collocation's frequency in a corpus is statistically significant. For a bigram w₁w₂, with corpus size N and unconditional probabilities P(w₁) = #w₁/N, P(w₂) = #w₂/N, the t-score is

t = (x̄ − μ) / √(s²/N),

where x̄ = #w₁w₂/N is the observed proportion, μ = P(w₁)·P(w₂) is the probability under the null hypothesis that the two words appear independently, and s² = x̄(1 − x̄) ≈ x̄. For large N the t-test reduces to a Z-test.

Lexicostatistics models lexical similarity between languages connected by a family, sprachbund, language contact, or other historical relation. Quantitative linguistics (QL) studies language learning, change, and structure statistically; its most ambitious goal is a general theory of language as a system of interrelated language laws, a programme for which synergetic linguistics was designed. Quantitative comparative linguistics combines lexicostatistics, glottochronology, and phylogenetic methods borrowed from biology.

Source: adapted from "Mathematical linguistics" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Mathematical_linguistics

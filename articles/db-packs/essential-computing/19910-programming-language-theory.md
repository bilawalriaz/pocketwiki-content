# Programming language theory

Programming language theory (PLT) is the branch of computer science that studies formal languages designed to be executed by machines. It asks what a program *means*, how that meaning can be reasoned about mathematically, and how languages should be classified and designed. The field borrows tools from linguistics, mathematics, and software engineering, and rests on one idea: programs are mathematical objects that can be described, transformed, and proved correct.

## Roots in the lambda calculus

The cornerstone is the **lambda calculus**, introduced by Alonzo Church (with Stephen Cole Kleene) in the 1930s as a model of computation. It encodes computation as pure functions and is sometimes called the world's first programming language, even though it was built to model thought, not to run on hardware. Modern functional languages such as Haskell, ML, and Lisp dialects are described as a "thin veneer" over lambda calculus. The lowercase Greek letter λ, taken from this calculus, is the field's unofficial symbol and appears on the cover of *Structure and Interpretation of Computer Programs* (Abelson and Sussman, 1985) and in the title of Steele and Sussman's *Lambda Papers* (1975–1980), which accompanied the design of Scheme.

## Historical development

Konrad Zuse designed Plankalkül in the 1940s, the first concrete programming language, though it stayed secret until 1972 and was not implemented until 1998. FORTRAN followed in 1954–1957 from John Backus's IBM team, the first widely used high-level language; its committee's successor produced ALGOL 58. John McCarthy created Lisp at MIT, the first academically successful language. Noam Chomsky's hierarchy of formal grammars gave the field a classification tool for syntax.

In the 1960s the field matured. Ole-Johan Dahl and Kristen Nygaard built Simula (1962), the first object-oriented language and the source of coroutines. Peter Landin showed lambda calculus can model real languages and introduced the SECD machine (1964) and ISWIM (1966), a conceptual ancestor of Haskell. Christopher Strachey formalised R-values, L-values, and parametric versus ad hoc polymorphism (1967). Tony Hoare published Hoare logic, a form of axiomatic semantics (1969). William Alvin Howard identified the Curry–Howard correspondence, linking proofs and typed programs (1969).

The 1970s added denotational semantics (Dana Scott, 1970), logic programming and Prolog (1972), Backus's 1977 Turing Award lecture proposing function-level programming, the Hindley–Milner type-inference algorithm for ML (Robin Milner, 1978), and Scheme (from 1975), a Lisp dialect with lexical scoping and first-class continuations. The 1980s brought structured operational semantics (Plotkin, 1981), process calculi for concurrency such as Milner's CCS, Hoare's CSP, and Hewitt's actor model, Miranda (1985) reviving lazy pure functional programming, and Haskell 1.0 in 1990. Bertrand Meyer codified design by contract in Eiffel. In the 1990s, monads entered practical functional programming through Eugenio Moggi and Philip Wadler.

## Sub-disciplines

**Formal semantics** specifies what programs mean. Three frameworks dominate: **denotational semantics** maps a program to a mathematical object; **operational semantics** describes a program by the steps an abstract machine takes; **axiomatic semantics** characterises a program through logical rules, as in Hoare logic.

**Type theory** studies type systems, syntactic methods that classify phrases by the values they compute so that certain errors become impossible at compile time. Languages are largely distinguished by their type discipline, and the Curry–Howard correspondence ties types to logical proofs.

**Program analysis and transformation** covers techniques for proving properties of programs and for translating between languages. **Compiler construction** splits that translation into syntax analysis (scanning and parsing), semantic analysis, optimisation, and code generation. **Run-time systems** study the supporting machinery: virtual machines, garbage collectors, and foreign-function interfaces.

**Comparative programming language analysis** groups languages into paradigms (functional, object-oriented, logic, concurrent) by their features. **Metaprogramming** lets programs write or manipulate other programs. **Domain-specific languages** are tailored to one problem area, trading generality for expressiveness there.

## Where the work is published

Research appears mostly at conferences: POPL (Principles of Programming Languages), PLDI (Language Design and Implementation), ICFP (Functional Programming), OOPSLA (Object-Oriented Programming), and ASPLOS (Architectural Support for Programming Languages). Peer-reviewed journals include *ACM TOPLAS*, the *Journal of Functional Programming*, the *Journal of Functional and Logic Programming*, and *Higher-Order and Symbolic Computation*.

PLT draws heavily on computability theory, category theory, and set theory to formalise what languages can express and what proofs about them are valid.

Source: adapted from "Programming language theory" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Programming_language_theory

# Knowledge-based systems

A knowledge-based system (KBS) is a computer program that reasons over an explicit store of facts to solve complex problems. It was a central focus of artificial intelligence research in the 1980s, though the label now covers a broad range of systems that share the same two-part structure: a **knowledge base** of domain facts and rules held outside the program's code, and an **inference engine** that applies general reasoning methods to those facts to derive new conclusions.

## Knowledge base and inference engine

A conventional program bakes its assumptions into procedural code; a knowledge-based system does not. The knowledge is written down separately, so it can be inspected, edited, and reasoned about by the program itself. Knowledge can be expressed as simple rules and assertions, or organised through richer structures such as a subsumption ontology, frames, conceptual graphs, or logical assertions. Structured representations matter because they let the system exploit relationships (for instance, that a robin is a bird) during reasoning rather than treating every fact as an isolated entry.

The inference engine is the part that does the thinking. Most commonly it uses **forward chaining**, starting from known facts and firing rules whose conditions are satisfied until no more conclusions can be drawn, or **backward chaining**, starting from a goal and working backwards to find supporting facts. More formal alternatives include automated theorem proving, logic programming, blackboard systems, and term-rewriting systems such as Constraint Handling Rules.

## Knowledge-based versus expert

The terms "knowledge-based system" and "expert system" were often used as synonyms, because nearly all of the first wave of KBSs were built for expert tasks. They actually describe different things. *Expert* describes the purpose: replacing or aiding a human expert on a task requiring specialised knowledge. *Knowledge-based* describes the architecture: knowledge held explicitly rather than woven into code. Almost every expert system is knowledge-based, while many knowledge-based systems are not designed as expert assistants.

## Rule-based systems and Mycin

The earliest knowledge-based systems were rule-based expert systems. Facts about the world were stored as simple assertions in a flat database, and domain-specific rules operated on those facts to add new ones. Mycin, an early medical-diagnosis program, is the classic example.

Storing knowledge as explicit rules brought three lasting advantages. **Acquisition and maintenance**: domain experts could often write and revise the rules themselves, without a programmer acting as intermediary. **Explanation**: because the chain of inferences is recorded, the system can show the user why it reached a conclusion, for example by listing the facts that led to a diagnosis. **General reasoning**: separating knowledge from the engine that processes it allowed general-purpose inference engines to draw conclusions that even the original rule authors had not anticipated.

## Meta-reasoning

Later architectures allowed the system to reason about its own reasoning. The BB1 blackboard architecture could monitor its problem-solving process and mix different strategies (top-down, bottom-up, opportunistic) depending on the current state. The problem-solver ran both a domain-level problem and its own control problem in parallel, with the two influencing each other. Other systems supporting this kind of meta-level reasoning include MRS, SOAR, and J. Pitrat's CAIA system. RefPerSys is an open-source project continuing this line of work through C++ code generation.

## Widening applications

Beyond diagnosis, knowledge-based systems spread through the 1980s and 1990s into real-time process control, intelligent tutoring systems, and specialised solvers for protein structure analysis, construction-site layout, and computer fault diagnosis. The common thread is that each application involves hard, knowledge-intensive decisions that benefit from explicit, inspectable rules.

## Richer representations: frames and classifiers

As systems grew more ambitious, the representations grew richer. Frames, introduced by Marvin Minsky in 1974, package world knowledge into data structures with named slots for attributes and relations, organised hierarchically through class-subclass links. Slots can hold values, defaults, constraints, and procedural attachments called daemons that fire when conditions are met, allowing structured knowledge to drive its own behaviour rather than relying solely on independent rules.

A second advance, the **classifier**, arrived in the 1990s. Rather than having a developer declare every subsumption relationship by hand, a classifier takes raw facts about the world and deduces how concepts relate, then uses those deduced relations to make further inferences. Classification thus doubles as a form of inference.

## The Semantic Web

The most recent step has been to apply knowledge-based technology, particularly a family of logic called description logic, to the internet. Web data is large, messy, and unstructured, and benefits from on-demand classification of objects rather than a rigid schema. The resulting vision, the **Semantic Web**, treats web content as machine-meaningful knowledge that can be reasoned over, drawing directly on the classification capability that classifiers brought to knowledge-based systems.

Source: adapted from "Knowledge-based systems" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Knowledge-based_systems

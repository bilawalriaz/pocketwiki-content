# Knowledge representation and reasoning

Knowledge representation (KR) is the branch of artificial intelligence concerned with encoding information about the world in a form a computer can use to solve complex tasks, from medical diagnosis to natural-language dialogue. Knowledge representation and reasoning (KRR, also KR&R or KR²) extends this by adding automated inference: the system stores knowledge and draws conclusions from it. The field borrows from psychology, to model how humans structure what they know, and from logic, to mechanize reasoning.

## Why a dedicated representation matters

Conventional procedural code forces developers to spell out every step, which becomes unmanageable as problems grow. A knowledge representation separates *what is known* from *what to do with it*, so domain experts can express rules ("if symptoms include X and Y, consider diagnosis Z") without writing control flow. This split yields the standard vocabulary still in use: a **knowledge base**, holding facts and rules about a domain, and an **inference engine**, which applies those rules to answer questions. Early expert systems in the 1970s and 80s adopted this architecture to match human competence on narrow tasks such as medical diagnosis.

## Formalisms and the logic versus procedures conflict

A formalism is the chosen vocabulary and structure for stating knowledge. Traditional formalisms include semantic networks, frames (abstract descriptions of categories with slots for data), rule-based systems, logic programs, and ontologies. Reasoning engines built on these include inference engines, theorem provers, model generators, and classifiers.

Two traditions dominated early work. **Logical representations**, anchored in first-order logic, used automated theorem provers such as John Alan Robinson's resolution method and John McCarthy and Pat Hayes' situation calculus for reasoning about actions. **Procedural representations**, advocated at MIT, embedded knowledge in procedures rather than declarative statements. The conflict resolved in the early 1970s with logic programming and Prolog, which used SLD resolution to treat Horn clauses as goal-reduction procedures, gaining the rigour of logic with an executable syntax.

Frames, introduced by Marvin Minsky in the mid-1970s, describe categories with slots, inheritance, and constraints, much like object classes. Once frame researchers and rule-based researchers recognized that frames handled structured real-world descriptions while rules handled complex diagnostic logic, integrated systems appeared. The 1983 Knowledge Engineering Environment (KEE) from Intellicorp combined a forward- and backward-chaining rule engine with a frame-based knowledge base with inheritance and message passing.

## The expressivity and tractability trade-off

First-order logic (FOL) is the standard yardstick for expressive power because it can formalise much of mathematics. Its drawbacks as a practical KR formalism are ease of use (complex notation, many ways to say the same thing) and efficiency (proof procedures are hard to implement efficiently). A key 1970s discovery was that languages lacking FOL's full expressive power, such as databases, semantic nets, and production systems, can offer nearly equivalent expressiveness while being far easier for developers and computers to handle. Rule-based expert systems, logic programming, and Prolog all sit on this balance point. Prolog in particular offers a rule-based syntax with well-defined logical semantics, something production rules lack.

## Classifiers and the Semantic Web

KL-ONE in the mid-1980s was a frame language with rigorous logical semantics and an automated reasoner called a classifier. A classifier analyses declarations in a knowledge base and infers new facts, such as promoting one class to a subclass of another, or checking that an ontology is consistent. Unlike rule-based reasoning, classification focuses on subsumption (the Is-A relation) rather than IF-THEN inference.

Classifier technology underpins the Semantic Web, the effort to add a layer of machine-readable meaning on top of the Internet. The Resource Description Framework (RDF) provides basic class, subclass, and property definitions; the Web Ontology Language (OWL) adds richer semantics and integrates with classification engines. The goal is to let users pose logical queries and retrieve pages that match concepts, not just keyword strings.

## Common-sense knowledge and Cyc

A persistent obstacle is that humans rely on vast background knowledge about physics, causality, and intention that is obvious to people but invisible to a machine. The frame problem captures a piece of this: in event-driven logic, one must explicitly state that objects stay where they are unless moved. Doug Lenat's Cyc project, beginning in the mid-1980s, attempted to encode common-sense knowledge about time, causality, physics, and intention in its own frame language (CycL), using large numbers of human analysts to document each domain.

## What a representation does

In a 1993 paper, Randall Davis and colleagues proposed five roles for any KR framework:

| Role | What it means |
|---|---|
| Surrogate | A stand-in for the world, so an agent can reason instead of acting |
| Ontological commitments | The vocabulary imposed on the world ("think in terms of X") |
| Theory of intelligent reasoning | What inferences the system sanctions and recommends |
| Medium for efficient computation | How the representation organises information to make those inferences cheap |
| Medium of human expression | A language in which people can say things about the world |

## Core design issues

Ron Brachman, writing in 1985, grouped the recurring difficulties in KR design into a set that still applies. **Primitives** are the underlying framework, ranging from semantic networks and frames to FOL-based languages such as Prolog. **Meta-representation**, or reflection, is a formalism's ability to inspect and modify its own structure at runtime, the same way a Smalltalk meta-object protocol lets programs reshape their class definitions. **Incompleteness** arises because classical logic demands extra axioms to handle the messy real world, so expert systems introduced certainty factors, later formalised as fuzzy logic. **Universals versus facts and defaults** is the tension between general statements ("all humans are mortal") and specific instances ("Socrates is human"), handled through universal and existential quantification and usually modelled with sets. **Non-monotonic reasoning** lets conclusions be retracted when underlying facts change, supported in rule-based systems by a truth maintenance system that tracks dependencies. **Expressive adequacy** and **reasoning efficiency** are linked: the more a formalism can express, the harder its inference engine is to run efficiently, since full FOL is theoretically undecidable in the general case.

## Ontology engineering

As knowledge bases grew from research demos to real applications, the field shifted toward ontology engineering: building large, modular ontologies that multiple projects could share. Tom Gruber observed that "every ontology is a treaty, a social agreement among people with common motive in sharing," because no single ontology can fit every domain. Examples include domain-specific ontologies for liquids, time, belief, and electronic circuits, each offering a particular way of carving up its subject matter.

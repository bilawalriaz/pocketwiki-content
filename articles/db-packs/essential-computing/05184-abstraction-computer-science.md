# Abstraction (computer science)

An abstraction is a simplified interface that exposes what matters and hides the details that do not. By raising the level at which a problem is expressed, it lets people build and reason about large systems one manageable step at a time.

## Why abstraction is necessary

Computing operates at a remove from the physical world. Hardware implements a model of computation interchangeable with other models, and software is built up in architectures that let humans focus on a few issues at once. These architectures are specific choices of abstractions. Greenspun's tenth rule notes that any sufficiently complex program ends up containing an ad hoc, informally specified, bug-ridden implementation of half of some abstract idea: such architectures are both inevitable and complex.

Programmer Joel Spolsky argued that all abstractions are leaky, meaning the lower-level details beneath them can never be fully hidden. The goal is not perfect hiding but reducing the number of concepts a programmer must hold in mind at once.

## Mechanisms of abstraction

**Language abstraction** is the central form. New artificial languages are developed to express specific aspects of a system, and computer languages can themselves be processed by a computer. The classic progression runs from first-generation machine language to second-generation assembly language to third-generation high-level languages, then onward into scripting and domain-specific languages. Each step raises the level of expression and serves as a stepping stone for the next.

Within a language, certain features let the programmer create new abstractions: subroutines (named reusable blocks of code), modules (independently compilable units), polymorphism (one interface accepting many underlying types), and software components. Design patterns and architectural styles are abstractions that live in the design of a system and remain invisible to a translator. A foreign function interface lets a higher-level language call into a lower-level one.

**Control abstraction** lets a programmer write `a := (1 + 2) * 5` instead of the long sequence of register and binary operations the hardware performs. Without it, every common task would be re-specified for every program and code would be tied to one particular instruction set.

**Data abstraction** separates a data type's abstract properties, the interface visible to client code, from its concrete implementation, kept private and changeable for efficiency. A lookup table that maps keys to values illustrates this: it may be a hash table, a binary search tree, or a linear list of pairs, yet client code sees the same behaviour in each case. The interface acts as a contract; anything not spelled out is subject to change without notice.

## Abstraction in object-oriented programming

In object-oriented programming, abstraction defines objects that represent abstract "actors" which can perform work, report and change their state, and communicate with other objects. Encapsulation hides state details; tying behaviour to data and standardising how different data types interact is where abstraction enters. When abstraction proceeds into operations so that objects of different types can be substituted, it is called polymorphism. When it proceeds inside types or classes to simplify a set of relationships, it is called inheritance or delegation.

Common Lisp Object System and Self use less of a class-instance distinction and rely more on delegation. C++ leans heavily on templates (compile-time type parameters) and overloading, which trades some flexibility for static efficiency. Deciding what to abstract is the central concern of object-oriented design; determining the relevant relationships in the real world is the concern of object-oriented analysis.

## Formal methods and soundness

In formal semantics, abstraction means considering a less detailed but safe definition of program behaviour, for instance observing only the final result of an execution rather than every intermediate step. An abstraction is exact for a property if the property can be answered equally well on the abstract or concrete model; for example, evaluating an integer expression modulo n requires only operations modulo n. An abstraction is sound if it cannot yield a false answer, even when it sometimes only answers "I don't know". Abstraction is the core concept of abstract interpretation, and model checking generally runs on abstract versions of the systems under study.

## Levels of abstraction

Computer science commonly organises systems into levels, each a different model of the same information with a different amount of detail. Each relatively abstract, "higher" level builds on a relatively concrete, "lower" level that offers a more granular representation. Gates build on electronic circuits, binary on gates, machine language on binary, programming languages on machine language, applications and operating systems on programming languages. Each level is embodied by, but not fully determined by, the level beneath it.

Database systems are a familiar three-level example. The physical level describes how data is actually stored. The logical level describes what data the database stores and the relationships among it, in simpler structures. The view level exposes only the part of the database a given user needs. This separation is called physical data independence: users of the logical level do not need to be aware of the underlying physical complexity. Layered architecture applies the same idea to software, hardware, and communications design, where components are isolated into layers so that a change in one layer does not affect the others.

Source: adapted from "Abstraction (computer science)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Abstraction_%28computer_science%29

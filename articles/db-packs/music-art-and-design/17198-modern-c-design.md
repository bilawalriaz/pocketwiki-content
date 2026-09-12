# Modern C++ Design

*Modern C++ Design: Generic Programming and Design Patterns Applied* is a 2001 book by Andrei Alexandrescu (Addison-Wesley, 323 pages). Scott Meyers called it "one of the most important C++ books." Alexandrescu did not invent template metaprogramming, but the book popularised it among working C++ programmers and introduced three now-common terms: *modern C++* (as distinct from older C/C++ style), *policy-based design*, and *typelist*.

The book pairs two things: design patterns expressed as compile-time C++ idioms, and a reference library called **Loki** that contains every example in working code. Loki was originally compatible only with CodeWarrior and Comeau C/C++; later work broadened it to Clang, GCC, Visual C++ 6.0, and Borland C++ Builder 6.0, and compiler vendors used Loki as a conformance benchmark. Maintenance moved to an open-source SourceForge project led by Peter Kümmel and Richard Sposato, and the library has since outgrown the book with components such as StrongPtr, Printf, and Scopeguard. Loki also inspired similar tools in Boost.

## Policy-based design

Policy-based design is the book's signature contribution. Alexandrescu described it as a compile-time variant of the **strategy pattern**, built on C++ template metaprogramming. It became closely associated with C++ and with D, because both need compilers with robust template support, which became common only around 2003. Earlier precedents include parametric modules (functors) in ML and C++ allocators as a memory-management policy.

The central structure is a **host class**: a class template that takes several type parameters and is instantiated with user-supplied **policy classes**. Each policy class implements one **policy**, an implicit interface, and each policy encapsulates one mostly orthogonal aspect of the host's behaviour. Mixing and matching canned policies yields an exponential number of behaviour combinations, resolved at compile time. Users can also supply a custom policy for behaviour the library does not anticipate. Even when only one implementation of each policy exists, decomposing a class into policies surfaces every orthogonal decision and forces modular design.

Policies differ from callbacks: a policy is a class, not a function, so it typically bundles several related methods plus state and nested types. The host class can be read as a metafunction that maps a set of behaviour-types to a single combined type.

Mechanically, a host class usually publicly inherits from each of its policies via **multiple inheritance**. Private inheritance or member containment also work, but public inheritance lets a policy add new methods that become part of the host's public interface without the host needing to know about them. This inversion is the key conceptual move: in OOP, abstract base classes define interfaces and derived classes implement them. In policy-based design the derived (host) class defines the interface and the base (policy) classes implement it. The public inheritance here is not an is-a relationship, which would be a design defect in OOP but is normal for policies.

Policies carry a structural cost: the policy interface is implicit, defined by duck typing rather than by any explicit declaration in code, so it must be documented in comments. The discipline is **commonality-variability analysis**: split a class into a fixed core (the policy-based class) and variable parts (the policies), and postpone every limiting design decision by delegating it to a named policy. Good policy sets group related customisation points (storage, validation, threading) into one argument rather than fragmenting them.

The **template method pattern** fits naturally: the host holds a skeleton algorithm that, at fixed customisation points, calls into the policies. C++20 **concepts** can express the same constraints explicitly, giving a library a way to state a policy's required interface in code instead of in comments.

## A minimal example

The source shows a contrived *Hello World* host class that takes two policies: `WriteToStdout`, supplying `write(string&&)`, and `EnglishMessage` or `GermanMessage`, each supplying a `message()` returning `"Hello, World!"` or `"Hallo Welt!"`. The host inherits from both, and its `run()` method calls `write(message())`. `HelloWorld<WriteToStdout, EnglishMessage>` prints English; swapping `EnglishMessage` for `GermanMessage` changes only the language policy. Adding a new output channel (file, network, log) means writing a new class with a `write` method and passing it as `OutputPolicy`.

## The Loki toolkit

Loki is Alexandrescu's accompanying library and doubles as the book's runnable spec. It relies heavily on template metaprogramming and supplies reusable components including **typelist**, **functor**, **singleton**, **smart pointer**, **object factory**, **visitor**, and **multimethods**. Because Loki pushed compilers hard on template conformance, vendors treated it as a benchmark, which raised the baseline of standard-conforming compilers across the industry.

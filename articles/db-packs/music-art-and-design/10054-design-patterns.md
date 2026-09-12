# Design Patterns

*Design Patterns: Elements of Reusable Object-Oriented Software* is a 1994 software engineering book by Erich Gamma, Richard Helm, Ralph Johnson, and John Vlissides, with a foreword by Grady Booch. Published by Addison-Wesley, it runs 395 pages and put software design patterns on the map. Both the book and its authors are known as the "Gang of Four" (GoF). More than 500,000 copies have sold in English and 13 other languages. In 2005, ACM SIGPLAN gave the authors its Programming Languages Achievement Award.

The project began at the 1990 OOPSLA conference, where Gamma and Helm met during a "Towards an Architecture Handbook" session; Johnson and Vlissides joined later.

## What the book argues

The first two chapters lay out principles for designing object-oriented software. Four ideas do most of the work.

**Program to an interface, not an implementation.** Client code depends on a contract of methods rather than a concrete class, so the client stays unaware of which class it has, as long as that class fulfils the interface. This enables dynamic binding and polymorphism, where different classes each supply their own version of the same method call.

**Favor object composition over class inheritance.** Composition builds new behaviour by combining objects with well-defined interfaces at runtime. The book calls this *black-box reuse*, because the internals of the composed objects stay hidden. Inheritance is *white-box reuse*: a subclass can see inside its parent, so changes in the parent ripple into the child. The authors warn that "inheritance breaks encapsulation" because any change to a parent's implementation can force subclasses to change too. They recommend inheriting mainly when reusing most of an existing component and adding only small amounts of new code.

**Delegation and parameterised types are powerful but costly.** Delegation is an extreme form of composition: a *sender* passes itself to a *delegate* so the delegate can call back through the sender, wiring two parts of a system together at runtime rather than at compile time. Parameterised types, generics in Java or C# and templates in C++, let code refer to types it does not yet know. The authors note that "dynamic, highly parameterised software is harder to understand and build than more static software."

**Aggregation versus acquaintance.** An *aggregate* owns its parts and shares their lifetime. An *acquaintance*, also called *association*, merely knows of another object and can call it without responsibility for it. Acquaintance implies looser coupling and is usually better for maintainability.

The authors also distinguish a *toolkit*, a class library, from a *framework*, cooperating classes that already dictate the skeleton of an application. Applications are hard to design, toolkits are harder, and frameworks are the hardest of all.

## The 23 patterns

The core of the book is a catalogue of 23 patterns grouped by intent. Each pattern names a recurring design problem and a reusable solution, giving designers a shared vocabulary for trade-offs.

**Creational patterns** control how objects are made, deferring or hiding which class gets instantiated.

| Pattern | What it does |
|---|---|
| Abstract factory | Groups related object factories under a common theme. |
| Builder | Separates how a complex object is built from how it is represented. |
| Factory method | Creates an object without committing to its exact class. |
| Prototype | Creates a new object by cloning an existing one. |
| Singleton | Restricts a class to exactly one instance. |

**Structural patterns** describe how classes and objects are composed.

| Pattern | What it does |
|---|---|
| Adapter | Wraps an existing class with a new interface so incompatible classes work together. |
| Bridge | Decouples an abstraction from its implementation so each varies independently. |
| Composite | Treats a group of similar objects and a single object the same way. |
| Decorator | Adds or overrides behaviour on a single object at runtime. |
| Facade | Exposes a simple interface to a large body of code. |
| Flyweight | Shares state across many similar objects to cut memory cost. |
| Proxy | Stands in for another object to control access, cut cost, or hide complexity. |

**Behavioural patterns** characterise communication and responsibility between objects.

| Pattern | What it does |
|---|---|
| Chain of responsibility | Passes a request along a chain until something handles it. |
| Command | Turns a request into an object containing the action and its parameters. |
| Interpreter | Implements the grammar of a specialised language. |
| Iterator | Walks through a collection without exposing how it is stored. |
| Mediator | Centralises how a set of classes interact so they need not know each other. |
| Memento | Captures an object's state so it can be restored later, enabling undo. |
| Observer | Lets many objects subscribe and react to an event. |
| State | Changes an object's behaviour when its internal state changes. |
| Strategy | Selects one algorithm from a family at runtime. |
| Template method | Fixes the skeleton of an algorithm in a base class, letting subclasses fill in steps. |
| Visitor | Moves operations on an object structure into a separate visitor object. |

## Criticism and influence

The book has been criticised on the ground that several patterns exist only to compensate for missing features in C++. Paul Graham argued that visible patterns in a program are a sign that the available abstractions are too weak, and that the author is hand-writing something a better language feature would generate. Peter Norvig showed that 16 of the 23 patterns are simpler or vanish entirely in dynamic languages like Lisp or Dylan. Hannemann and Kiczales later showed that 17 of the 23 patterns shed their cross-code dependencies when re-implemented in the aspect-oriented language AspectJ, which lets a programmer declare cross-cutting concerns separately from the main code.

In a 2009 interview, Gamma said the authors met in 2005 to consider a revision. They would recategorise some patterns and add new ones, including extension object/interface, dependency injection, type object, and null object. Gamma wanted to drop Singleton but could not get consensus.

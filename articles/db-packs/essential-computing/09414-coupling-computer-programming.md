# Coupling (computer programming)

In software engineering, coupling is the degree of interdependence between software modules: how closely two routines are connected and how strongly their relationships bind them. Larry Constantine introduced the metric in the late 1960s as part of structured design, formalised in Stevens, Myers & Constantine (1974) and Yourdon & Constantine (1979), and it has remained a standard measure of software quality.

## Coupling and cohesion

Coupling is usually contrasted with cohesion. Cohesion describes how related the functions inside a single module are; coupling describes how dependent modules are on each other. Low coupling often correlates with high cohesion, and together they indicate a readable, maintainable system.

## Degrees of coupling

Coupling is not binary. It ranges from "low" (loose, weak) to "high" (tight, strong) and is multi-dimensional. Gregor Hohpe lists dimensions including technology, location, topology, data format and type, semantic content, conversation pattern, order, and timing.

### Procedural coupling types, highest to lowest

Content coupling (highest): one module uses the code of another, for example by branching into it. This violates information hiding, the principle that a module should keep its internals private.

Common coupling: several modules share the same global data. A change to that data can cause uncontrolled error propagation and unforeseen side effects wherever it is read or written.

External coupling: two modules share an externally imposed data format, communication protocol, or device interface, typically when communicating with external tools.

Control coupling: one module controls the flow of another by passing it information about what to do, such as a flag that selects a behaviour.

Stamp coupling (data-structured coupling): modules share a composite data structure but use only part of it. Returning a full `UserProfile` object when a consumer needs one attribute is a classic example. Changing an unused field can still force every consumer to be re-tested, and the extra payload wastes bandwidth at scale.

Data coupling (lowest): modules share only elementary data through parameters, such as passing an integer to a square root function. Each piece is small and self-contained.

### Object-oriented and other paradigms

In object-oriented programming, subclass coupling describes a child class depending on its parent; the parent does not depend on the child. Temporal coupling bundles actions into one module simply because they happen at the same time, not because they are logically related. Dynamic coupling is measured at runtime, because static metrics lose precision under heavy use of dynamic binding or inheritance. Semantic coupling uses latent semantic indexing (a statistical method that scores textual similarity) over comments and identifiers to estimate conceptual similarity between entities. Logical coupling, also called evolutionary or change coupling, finds modules that tend to be changed together by analysing release history.

## Why tight coupling causes problems

Tightly coupled systems tend to develop these weaknesses: a change in one module usually forces a ripple effect through others; assembling modules takes more effort because each drags in its dependencies; a module is harder to reuse or test in isolation when its dependencies must come along; and message-handling costs (creation, transmission, translation, and interpretation) grow with message length and complexity, with formats like SOAP adding parser overhead.

## Reducing coupling

Functional design limits each module to a single responsibility, which naturally lowers its connections. Coupling between two classes A and B increases when A holds a reference to B, calls a service on B, references B in a method signature, or is a subclass or implementation of B. The goal of low coupling is that one module interacts with another only through a simple, stable interface and never needs to know the other's internals, the same idea behind information hiding. Middleware such as CORBA and COM lets objects communicate across implementations and across programming languages.

## Connascence

Connascence, introduced by Meilir Page-Jones, analyses the same dependencies coupling describes but along three dimensions: strength (effort required to refactor the dependency), locality (how close dependent components sit in the codebase), and degree (how many components are affected). It splits into static forms, visible at compile time such as method signatures, and dynamic forms, visible only at runtime such as timing, value, or algorithm dependencies. Common types include connascence of name, type, position, and meaning; name is generally weaker and easier to refactor than meaning, and position is fragile because reordering parameters breaks callers. Each traditional coupling type can manifest as several connascence types, and modern practices such as dependency injection and interface-based programming target these dependencies directly to lower strength and improve maintainability.

## Quantitative metric

A widely cited formula expresses coupling numerically for a single module:

```
C = 1 − 1 / (d_i + 2·c_i + d_o + 2·c_o + g_d + 2·g_c + w + r)
```

`d_i` and `d_o` count input and output data parameters, `c_i` and `c_o` count input and output control parameters, `g_d` and `g_c` count global variables used for data and control, `w` is fan-out (modules called), and `r` is fan-in (modules calling this one). Control and global variables are weighted by 2 because they couple more strongly than plain data parameters. The result ranges from about 0.67 for a module with one input, one output, and a fan-out of 1, toward 1.0 as parameters, globals, and call relationships accumulate.

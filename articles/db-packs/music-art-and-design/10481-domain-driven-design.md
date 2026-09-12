# Domain-driven design

Domain-driven design (DDD) is a software design approach that builds software around a model of the business domain it serves, shaped by ongoing collaboration with that domain's experts. Coined by Eric Evans in his 2003 book of the same name, it rejects one unified model for a large system. The system is split into bounded contexts, each with its own model whose vocabulary matches the business it represents: a loan-processing system would have classes like `loan application` and `customers`, and methods like `accept offer` and `withdraw`.

The goal is to keep the primary focus on the core domain and its logic, base complex designs on a domain model, and refine a shared conceptual model through creative collaboration between developers and domain experts. Microsoft recommends DDD only for complex domains where the model genuinely clarifies a common understanding; critics note that maintaining a clean model demands significant isolation and encapsulation.

## Building blocks of the model

A domain model is a system of abstractions describing selected aspects of a domain. DDD recognizes several kinds:

- **Entity** — defined by its identity rather than its attributes, like an airline seat identified by a unique flight-and-seat number.
- **Value object** — an immutable object defined purely by its attributes, with no conceptual identity, like a business card whose only importance is the information printed on it.
- **Domain event** — a record of something that happened in the past that domain experts care about.
- **Aggregate** — a cluster of entities and value objects bound under a root entity. Outside objects may reference the root but not the other members. The root enforces consistency across the cluster, the way a driver steers a car without separately controlling each wheel, engine, and headlight.
- **Repository, factory, service** — repositories retrieve domain objects from storage, factories create them, and services carry out operations that do not belong to any single object.

Strategic design draws the boundaries between bounded contexts; tactical design shapes the model inside each one. In an object-oriented multilayered architecture, the domain layer is where this model lives, separate from infrastructure and application concerns.

## The ubiquitous language

The structure and naming of the code (class names, methods, variables) should match the business domain, forming a ubiquitous language shared by domain experts, users, and developers. This language is used inside the domain model, in requirements discussions, and in the code itself, so a term means the same thing to everyone.

## Events: domain versus integration

Yan Cui distinguishes two event categories that behave differently. Domain events signify important occurrences within a single bounded context, carry light payloads, and are consumed by listeners in the same service. Integration events communicate changes across bounded contexts to keep data consistent across the system, and tend to carry richer payloads because listeners in other contexts have less predictable needs, often leading to deliberately over-shared information.

## Context mapping

Context mapping defines how bounded contexts relate. Eric Evans lists several patterns: Partnership, where two teams commit to coordinated planning because they will succeed or fail together; Shared Kernel, a small subset of the model both teams maintain jointly; Customer/Supplier Development, a clear upstream-downstream relationship; Conformist, where a downstream team accepts the upstream model without translation; Anticorruption Layer, which translates the upstream model into the downstream team's own terms; Open-host Service, a published protocol for integrating one subsystem with many; Published Language, a shared format for exchanging domain information such as an industry data interchange standard; Separate Ways, where two contexts share nothing; and Big Ball of Mud, a pragmatic boundary drawn around an existing system that has no real internal structure.

## Relationship to other practices

DDD is often associated with Plain Old Java Objects and Plain Old CLR Objects, which express domain behavior without leaning on a specific framework. The naked objects pattern pushes this further by making the user interface a direct reflection of the domain model, on the assumption that a bad interface will force a better model. Domain-specific modeling applies DDD with domain-specific languages, and aspect-oriented programming separates technical concerns (security, transactions, logging) from the business logic. Model-driven engineering and model-driven architecture are compatible with DDD but have a different intent: they focus on translating a model into code for different platforms rather than defining a better domain model, although their model transformation and code generation techniques can carry a DDD model into a running system.

## CQRS, event sourcing, and microservices

Command Query Responsibility Segregation (CQRS), derived from Bertrand Meyer's Command and Query Separation, splits reads (queries) from writes (commands). A command mutates state by invoking a method on an aggregate root, which yields either a failure or a new state for persistence; queries only read. Event sourcing extends this by storing state as a sequence of events in an event store rather than as direct serialization. Aggregate roots validate commands and publish resulting events, often through a message broker. Because the aggregate root fully hides its internal state, formal tools like theorem provers apply more easily, and conflicts in distributed systems are resolved through optimistic concurrency keyed to the aggregate's version.

A bounded context often maps one-to-one onto a microservice, which keeps boundaries clean and supports independent deployment and scaling. One-to-many and many-to-one mappings are also used when scalability or operational simplicity demand it.

## Discovering the model

Event storming is a workshop technique that often precedes DDD. Stakeholders, domain experts, and developers use color-coded sticky notes to map domain events, their causes, and their effects, surfacing subdomains, bounded contexts, and aggregate boundaries before any code is written.

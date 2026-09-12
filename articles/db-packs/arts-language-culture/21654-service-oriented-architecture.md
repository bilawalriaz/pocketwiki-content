# Service-oriented architecture

Service-oriented architecture (SOA) is a software design style that builds applications from discrete, independently maintained services rather than a single monolithic program. Each service is a self-contained unit of functionality that exposes a formal interface, hides its internals as a black box, and can be called over a network by other services or clients. Applications are assembled by combining services, much as modular code is assembled from functions. SOA fits naturally into system integration, where existing capabilities must be reused and connected across boundaries.

## What a service is

A service logically represents a repeatable business activity with a specified outcome. It is self-contained, opaque to its consumer, and may itself be composed of other services. The same service can be reused by many applications without modification. A collection of cooperating services forms a service mesh, which delivers the behavior of a large application.

SOA is closely related to the idea of an API. An API can be thought of as the service itself; SOA is the surrounding architecture that lets the service operate. SOA must not be confused with Service-Based Architecture, a distinct style.

## How services communicate

Services exchange messages through a communication protocol over a network, typically an IP network. Messages carry metadata that describes both the functional behavior of the service and quality-of-service characteristics. Consumers pass data in a well-defined shared format or coordinate activities with other services. To remain independent of any vendor or technology, services interoperate through a formal contract, such as a WSDL interface, allowing, for example, a C# service on .NET and a Java service on Java EE to be consumed by the same application. SOA can also wrap legacy systems, including COBOL, and present them as network-callable services.

SOA sits on a continuum from earlier distributed computing and modular programming, through mashups and software as a service, to cloud computing, which some see as a descendant of SOA.

## Core principles

There are no universally mandated standards for SOA, though common principles include a standardized service contract shared across consumers; loose coupling, meaning reference autonomy and location transparency; longevity, so a service works today and tomorrow without forcing consumer changes; abstraction and autonomy, so services act as black boxes controlling their own functionality; statelessness, returning a value or an exception and minimizing retained state; appropriate granularity; composability, discovery through metadata, reusability, and encapsulation of code that predates SOA. These principles promote reuse at the macro level of services rather than at the level of individual classes and simplify interconnection with existing IT assets.

## Roles and composition

Each building block in SOA plays one of three roles. The service provider creates a service and publishes its description. The service broker, registry, or repository makes that description available to anyone who might call it; UDDI was an early, now-unsupported attempt at such discovery. The service requester or consumer looks up entries in the registry and binds to the provider to invoke the service. Their relationship is governed by the standardized service contract, which carries business, functional, and technical parts.

When several services are combined, two high-level styles apply: choreography, where services coordinate by exchanging messages without a central controller, and orchestration, where one service directs the others.

## Implementation approaches

SOA can be implemented with web services or microservices. SOAP, recommended by the W3C in version 1.2 in 2003, and WSDL give broad interoperability. Other technologies include Jini, CORBA, REST, gRPC, Apache Thrift, WCF, DDS, and OPC-UA, along with messaging systems such as ActiveMQ, JMS, and RabbitMQ. Specifications such as BPEL, WS-CDL, and WS-Coordination orchestrate fine-grained services into coarser-grained business services for workflows and composite applications.

Microservices are a modern interpretation of SOA, popular since 2014 alongside DevOps. Each microservice is an independently deployable process that communicates over the network through technology-agnostic protocols, enabling fine-grained interfaces, polyglot programming and persistence, lightweight container deployment, decentralized continuous delivery, and holistic service monitoring.

## Benefits and criticisms

Enterprise architects argue that SOA helps organizations respond more quickly to changing markets by promoting service-level reuse, simplifying connections to legacy systems, and enforcing shared standards. Services can be delivered and improved independently of larger, slower projects, shortening time-to-market. Testing is simplified because services are autonomous, stateless, and documented through stable interfaces; regression tests can be built around stubs.

SOA has also attracted criticism. It is often conflated with web services, which are only one implementation; XML- or JSON-based exchanges can impose overheads, though JBI, WCF, DDS, and binary XML formats such as VTD-XML reduce this cost. Stateful services force providers and consumers to share consumer-specific context, which reduces scalability and makes switching providers harder. Metadata management is difficult because many services exchanging millions of messages create complex trust relationships across organizations, and no uniform testing framework exists for the heterogeneous mix of services and continuously evolving platforms.

# Domain engineering

Domain engineering is the practice of building new software systems by reusing knowledge and assets gathered from previous systems in the same field. Most organisations operate in only a few **domains**, fields of activity such as banking, avionics, or medical imaging, and repeatedly produce similar systems with small variations for different customers. Domain engineering captures what those systems share and how they differ, then uses that knowledge to build new members of the family faster and at higher quality.

A closely related discipline is **product line engineering**, formalised in ISO 26550:2015, where domain engineering is paired with **application engineering**, which handles the life cycle of each individual product derived from the shared base.

## Phases

Domain engineering is organised into three phases that mirror the classic analysis–design–implementation stages, but applied to a **family of systems** rather than a single product. The output of each phase feeds both the next phase of domain engineering and the corresponding phase of application engineering, so reusable artefacts arrive where they are needed.

## Domain analysis

The first phase, **domain analysis**, defines the boundary of the domain, gathers information about it, and produces a **domain model** that records the commonalities and variabilities among systems in that field. Inputs come from existing systems, their design and requirements documents, user manuals, published standards, and customers.

The central tool is a **feature model**, introduced in feature-oriented domain analysis, which decomposes each system into required and optional features. Selecting features from this model lets engineers make reuse decisions very early, long before code is written. The resulting domain model captures not only features but also the vocabulary, concepts, and phenomena of the field, giving later developers a shared language and a reference for resolving ambiguity.

Domain analysis differs from ordinary **requirements engineering**, which gathers what one specific system must do, in two ways. It includes a creative step that pushes beyond what is already known, categorising similarities and differences and exposing new configuration points. It also produces **configurable** requirements and architectures, not the static specifications a single-project approach would yield.

## Domain design

The second phase, **domain design**, takes the domain model and produces a generic architecture to which every system in the family can conform. Where application engineering turns functional and non-functional requirements into a design for one system, domain design turns configurable requirements into a configurable, standardised solution for the whole family.

The core artefacts are **architectural patterns**: recurring structures that solve a problem common to many systems in the domain, even when their requirement configurations differ. A useful pattern must be both frequently recurring and of high quality, and its **scope of context** must be carefully bounded. Too much context makes a pattern inapplicable outside a narrow setting; too little leaves it too weak to be useful. The architecture must be flexible enough to satisfy every member of the family yet rigid enough to provide a solid framework.

## Domain implementation

The third phase, **domain implementation**, creates the process and tools for efficiently generating a customised program in the domain. Outputs include reusable components, a **domain-specific language** (a small language tailored to one problem area), or an application generator that assembles a concrete product from the configurable assets. One cited study found that adopting a domain-specific language cut the number of methods and symbols in the code by over 50% and the total lines of code by nearly 75%, with savings visible even during implementation. The same approach now reaches beyond traditional software: deep chains of web services and Internet-of-Things platforms behave like families of related services in which one organisation's component becomes another's reusable platform.

## Limitation

Domain engineering has been criticised for overemphasising **engineering-for-reuse** and **engineering-with-reuse** of generic features at the expense of **engineering-for-use**, in which an individual user's world-view, language, and context shape the design. Critics argue that the focus on generic, reusable assets can crowd out attention to the specific situation of the people who will actually use the system.

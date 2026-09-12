# Behavior-driven development

Behavior-driven development (BDD) is an agile software method built around collaboration between business and technical people. Its core objective is a shared understanding of the problem before any code is written, especially when the problem space is complex. BDD combines ideas from test-driven development (TDD), domain-driven design, and object-oriented analysis and design, giving developers, testers, and business stakeholders a common language and process.

A common misconception is that BDD is just a refinement of TDD. Although it was originally derived from TDD, its purpose is to capture requirements in a Business Language that uses real data and is Intention-revealing, Essential, and Focused (the BRIEF criterion). TDD is a discipline for writing tests; BDD is a discipline for discovering and stating what the software should do.

## How BDD works

BDD converts natural-language statements, written in a domain-specific language (DSL), into executable tests. Those tests double as the requirements, producing living documentation that stays in sync with the code. The DSL is the *ubiquitous language* borrowed from domain-driven design: a shared, semi-formal language used by every role on the team, both to discuss the domain and to write the specifications. The formality matters because the same sentences have to be readable by a business analyst and parseable by a tool.

BDD is an "outside-in" activity. Tests are named in terms of the desired behavior the business cares about, then progressively broken down toward the technical details. TDD makes no such distinction between high-level requirements and low-level details, so BDD can be seen as a more specific choice about what tests should describe.

## The user-story format

A BDD user story has three parts:

- **Title** — an explicit name for the story.
- **Narrative** — written as *As a* [role], *I want* [feature], *so that* [benefit].
- **Acceptance criteria** — one or more scenarios, each written as *Given* [initial context], *When* [event], *Then* [expected outcome], with optional *And* clauses.

Scenarios should be phrased declaratively, in business language, with no reference to UI elements. The most widely used syntax for this format is the Gherkin language used by the Cucumber tool. Teams are free to pick a standardized form, but BDD requires that they pick one and stick to it.

## Tooling and execution

A BDD tool is a testing framework bound to the ubiquitous language, unlike a TDD tool, which is largely free-format. The general process is:

1. The tool reads the specification document.
2. It parses the formal parts of the language (the *Given*, *When*, *Then* keywords) into clauses.
3. Each clause is mapped, by the developers, to a parameter in a test implementation.
4. The framework runs the tests, one per scenario, using those parameters.

Because BDD requires both a human-readable document and test code, the workflow is more laborious than pure TDD. Proponents argue the readability makes the documents useful as requirements specifications for non-technical audiences, which justifies the extra cost.

## Story-based versus specification-based BDD

Most BDD uses user stories as input. A less common subcategory, specification-based BDD, takes functional specifications of units (for example, a stack) instead of user stories. A stack specification reads like a list of *When/Then* rules for the component being tested. Such a specification is precise and unit-test-like but is less meaningful to a business user, so in practice it complements story-based BDD and operates at a lower level, often as a stand-in for free-format unit testing.

## The three amigos

A "three amigos" meeting, also called a Specification Workshop, is where the product owner, a developer, and a tester discuss a requirement through concrete examples. The goal is to surface missing specifications and converge on a shared understanding before implementation. Each role has a distinct job: the business representative defines the problem without proposing a solution, the developer proposes ways to solve it, and the tester questions the proposed solution by exploring "what if" scenarios to push the requirement toward precision.

# Go (programming language)

Go is a statically typed, compiled programming language created at Google by Robert Griesemer, Rob Pike, and Ken Thompson and publicly released on November 10, 2009. Often called "Golang," it was designed for multicore processors, networked servers, and large codebases, combining the runtime efficiency of C with the readability of dynamically typed languages like Python. The designers' shared dislike of C++ pushed the design toward omission: implementation inheritance, pointer arithmetic, implicit type conversions, assertions, and tagged unions are all absent. The specification is short enough to hold in a programmer's head, with only twenty-five reserved words. Features were included only when all three designers agreed; Pike summarized the intent as "less is exponentially more."

Version 1.0 shipped in March 2012. The current stable release is 1.27.0 (August 2026). Go 1 guarantees backward compatibility, and every release through 1.27 has kept that promise. Each major version is supported until two newer major releases appear. The team plans never to ship a 2.0, preferring long-term stability over breaking changes.

## Type system

Go's type system is mostly nominal: a `type` declaration defines a new named type distinct from others with the same underlying layout, and conversions between named types must be explicit. Functions can return multiple values, so the conventional way to report failure is to return a result together with an `error`.

Interfaces replace class inheritance. An interface lists required methods by name and signature, and any type that defines those methods implicitly satisfies the interface; there is no `implements` keyword. For example, a `Square` struct with an `Area() float64` method automatically satisfies a `Shape` interface wherever one is required. The compiler checks conformance statically, so the Go authors prefer the term "structural typing" over "duck typing." The empty interface `interface{}` (aliased as `any`) refers to a value of any type and is commonly used for generic containers and decoding JSON.

Since version 1.18 (March 2022), Go supports generics through type parameters declared in square brackets. The compiler substitutes concrete types at instantiation. Type sets expressed with `|` and the underlying-type operator `~` constrain which types a parameter accepts.

## Goroutines and channels

The defining technical feature of Go is its built-in concurrency model, derived from Tony Hoare's communicating sequential processes (CSP). A goroutine is a lightweight thread managed by the Go runtime; starting one is as simple as `go someFunction()`. The runtime multiplexes many goroutines onto a small pool of operating-system threads, scheduling work across available CPU cores automatically.

Goroutines coordinate through channels, which are typed conduits for messages. The expression `<-ch` receives a value (blocking until one arrives), and `ch <- x` sends one. A `select` statement waits on multiple channels at once, proceeding when any is ready. Channels may be buffered, allowing sends to proceed without a ready receiver.

The official guideline is "do not communicate by sharing memory; share memory by communicating." In practice, data races remain possible because all goroutines share a single address space. The runtime includes an optional race detector (available since Go 1.1) that flags unsynchronized access at execution time, and since Go 1.6 the map type is checked by default. Go provides no built-in safe-concurrency guarantee and instead relies on convention: passing a mutable value across a channel often signals a transfer of ownership.

## Tooling and omissions

The standard distribution ships a complete toolchain: `go build` compiles without separate makefiles, `go test` runs unit tests and benchmarks, `go fmt` enforces a single canonical code style, `go vet` performs static analysis, `go mod` manages dependencies, and `gopls` provides IDE features. Code formatting is mandatory; `gofmt` rewrites files automatically using tabs for indentation. The compiler enforces rules that are mere advice in other languages: no unused variables or imports, no cyclic dependencies.

The compiler produces statically linked binaries by default, embedding the Go runtime. The `net/http`, `testing`, `fmt`, and `encoding/json` packages are part of the standard library. Errors cross package boundaries through multi-value returns carrying an `error`, while a `panic`/`recover` mechanism handles unrecoverable conditions. Visibility is governed by capitalization: `Foo` is exported, `foo` is private to its package.

## Adoption

Go powers much of modern cloud infrastructure: Docker, Kubernetes, CockroachDB, Caddy, and Hugo are written in Go, and TypeScript 7 is written in Go. The language was named TIOBE Programming Language of the Year in 2009 (its first year) and again in 2016. TIOBE rankings fluctuated, dropping below fiftieth in 2015 before climbing back near the top by 2017, tracking Go's adoption in backend services and DevOps tooling.

Source: adapted from "Go (programming language)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Go_%28programming_language%29

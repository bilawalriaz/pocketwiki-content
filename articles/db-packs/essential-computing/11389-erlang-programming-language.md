# Erlang (programming language)

Erlang is a concurrent, functional programming language built around lightweight processes that communicate only by asynchronous message passing. It was designed at Ericsson in 1986 by Joe Armstrong, Robert Virding, and Mike Williams for telephone switches that must run for years without stopping, and those same properties now underpin messaging backends, databases, and other large-scale distributed systems.

## Runtime and OTP

The term Erlang usually refers to Erlang/OTP, the Open Telecom Platform, which combines the runtime with libraries and design principles. The runtime targets distributed, fault-tolerant, soft real-time systems that are highly available, nonstop, and support hot code swapping. Erlang's sequential subset uses eager evaluation, single assignment, and dynamic typing. The official implementation runs on the BEAM virtual machine, which compiles Erlang to threaded bytecode and, on most platforms, to native code via HiPE.

## Processes

Everything in Erlang is a process. An Erlang process is not an operating-system process or thread but a lightweight task scheduled by BEAM, with a per-process heap and garbage collector and an overhead near 300 words. A 2005 benchmark ran 20 million processes on a 64-bit node with 16 GB of RAM at roughly 800 bytes per process. Symmetric multiprocessing across cores has been supported since R11B in May 2006.

Processes are strongly isolated and share no memory. They interact solely by sending messages: a sender uses `!` to enqueue any Erlang term into the receiver's mailbox, and a receiver uses `receive` to pattern-match messages and consume one. Because no state is shared, explicit locks are unnecessary; the VM uses internal locking only. Messages can also be sent to processes on other nodes, and the same code works because location transparency hides the difference between local and remote communication. The model parallels CSP and occam, but is recast in a functional framework.

## Let it crash and supervisors

Erlang's error handling prefers to let a failing process die and be restarted rather than defend against every possible error inline. A supervisor process monitors its children and reacts to `'DOWN'` messages; if a worker crashes, the supervisor restarts it. Supervisor and worker processes can be nested to any depth, giving applications a fault-tolerant structure. This is practical because processes are cheap to spawn and discard. Joe Armstrong's summary of the process model: everything is a process, processes are strongly isolated, creation and destruction are lightweight, message passing is the only interaction, processes have unique names, and processes either do what they are supposed to or fail.

## Hot code loading

Erlang modules can be replaced at runtime. The VM keeps two versions of a module in memory at once; a process continues with the old version until it next makes an external call, at which point it picks up the new code. Updates are staged through explicit `code_switch` entry points so state can be reshaped between versions.

## Data types and syntax

Erlang has eight primitive types: integers with arbitrary-precision exact arithmetic, IEEE 754 64-bit floats, atoms (named constants, never garbage collected), references (globally unique values from `make_ref/0`), binaries (compact byte sequences), pids (process identifiers from `spawn/3`), ports (handles to external resources), and funs (function closures). Three compound types sit on top: fixed-size tuples with constant-time field access, lists built as `[Head|Tail]`, and maps with arbitrary key-value associations. Strings are syntactic sugar for lists of Unicode code points.

Programs are organised as modules in `.erl` files, with `-export` listing public functions. A function consists of pattern-matching clauses separated by `;`, ending in `.`. A clause can carry a guard such as `when N > 0, is_integer(N)`. Quicksort uses list comprehensions like `[X || X <- Rest, Smaller(X, Pivot)]`, read as "the list of X drawn from Rest where Smaller(X, Pivot) is true."

## History

Erlang was first implemented in Prolog and influenced by Ericsson's earlier PLEX language. By 1988 it had proven suitable for prototyping telephone exchanges, but the Prolog interpreter needed roughly a 40× speedup for production. Work on the BEAM VM began in 1992 to deliver that. Erlang reached production after the 1995 collapse of the AXE-N telephone exchange, when Ericsson chose it for the AXD ATM switch; the AXD301, announced in 1998, ran over a million lines of Erlang and reported nine-nines availability. In February 1998 Ericsson banned Erlang for new in-house products, prompting a December 1998 open-source release; most of the Erlang team then left to form Bluetail AB. Ericsson lifted the ban and re-hired Armstrong in 2004. Symmetric multiprocessing arrived in 2006.

## Use and influence

Erlang runs inside Ericsson's support nodes and in GPRS, 3G, and LTE networks, and is used by Nortel and Deutsche Telekom. WhatsApp is built on Erlang, and RabbitMQ and Ejabberd (an XMPP server) are written in it. Elixir compiles to BEAM bytecode, and other BEAM languages include Luerl, Lisp Flavored Erlang, and Gleam. Since open-sourcing, Erlang has spread into FinTech, gaming, healthcare, automotive, IoT, and blockchain, with named users including Goldman Sachs, Nintendo, AdRoll, Grindr, and Samsung.

# Memory management

Memory management is the way a computer system divides its memory among running programs and reclaims memory they no longer need. It exists because modern systems run more than one process at once. A *process* is a running program, and each one needs its own slice of memory while sharing a finite amount of physical RAM. Inside the system's *address space* — the range of memory addresses a process can use — two questions must be answered for every byte: where it lives in physical hardware, and how long it stays allocated.

## Virtual memory: decoupling addresses from hardware

Virtual memory answers the first question. Processes work with virtual addresses that hardware translates into real physical addresses on every memory access. The program behaves as if it owned a large, private address space even when actual RAM is much smaller. Pages not currently in use can be parked on disk and brought back into RAM on demand, a process called *paging* or *swapping*.

Virtual memory also enables *memory protection*: hardware checks every access against permissions, so one process cannot read or write memory belonging to another. This stops a bug or malicious code in one program from corrupting the rest of the system. Processes that genuinely need to exchange information can be given a shared region; shared memory is one of the fastest techniques for inter-process communication.

Memory is split into *primary storage* (fast, scarce RAM) and *secondary storage* (larger, slower disk), and the memory management system shuffles data between the two so frequently used material stays in primary storage.

## Manual memory management

Inside a single process's address space, allocation takes two forms: manual and automatic.

In manual memory management the programmer controls everything. A region called the *heap* holds blocks that have been allocated but not yet freed. In C, `malloc` carves out a block and `free` returns one. Several things go wrong. *External fragmentation* scatters small gaps between live blocks so a request cannot be satisfied even though enough total memory is free. Per-block bookkeeping inflates small allocations, so many systems combine tiny requests into *chunks*. The allocator must track every live block so two allocations do not overlap and no block is ever lost — a failure mode called a *memory leak*.

A 1994 study by Digital Equipment Corporation measured allocator cost. The fastest allocator examined needed an average of 52 instructions per slot, so the algorithm choice has measurable effects on program speed.

Common manual strategies:

- *Fixed-size blocks* (memory pools): hand out blocks of one size from a free list. Fast and free of internal fragmentation within a size, but wasteful when objects vary widely.
- *Buddy allocation*: keep separate pools for blocks whose sizes are powers of two. To allocate, take the smallest pool large enough and split a block in half, recording the two halves as "buddies". When both buddies of a block are free, merge them back into a larger block. Merging is fast and predictable.
- *Slab allocation*: pre-allocate caches sized for specific object types so any free slot fits any object of that type, reducing fragmentation.
- *Stack allocation* via `alloca`: instead of using the heap, the function grows the call stack and the memory is reclaimed when the function returns. It is fast but risks a stack overflow, and because `alloca` is not part of the C standard or POSIX, its overflow behavior is undefined. Microsoft Windows provides `_malloca`, which reports errors, and glibc can emulate it.

## Automatic memory management

Manual allocation is error-prone, so many systems automate parts of it.

Local variables in a function are the easiest case. When a function is called, the runtime carves out space on the *call stack* for its local variables; when the function returns, that space is released automatically. Special declarations can make those variables keep their values between calls, but the basic mechanism — space for the call, gone after — is what makes recursion possible.

*Garbage collection* is the more general approach: a runtime periodically finds objects the program can no longer reach and returns their memory to the free pool. It removes a large class of bugs but costs processor time and memory of its own.

*Reference counting* is a lighter alternative: every object carries a count of pointers that refer to it, and the count drops as references disappear. When it reaches zero, the object is freed. It is cheap and immediate, but a cycle — A points to B, B points to A — keeps both counts above zero forever, which leaks memory. *Weak references*, pointers that observe without affecting the count, or a hybrid that falls back to tracing garbage collection break these cycles.

*Memory pools* tie deallocation to a phase of the program. A web service, for instance, allocates heavily while handling a request and knows that everything allocated during that request can be discarded when the response is sent. Instead of tracking individual objects, it frees the whole pool at the boundary between requests.

## Historical designs

Burroughs shipped the first commercial implementation of virtual memory with the B5000 in 1961, integrating it into the hardware so no external memory management unit was needed. IBM's System/360, in contrast, had no virtual memory except on the Model 67. It used *protection keys* to isolate jobs — key 0 for the supervisor and keys 1–15 for user jobs — with regions, subpools, and control blocks tracking allocated and free storage inside each job. These two designs, full virtual addressing built into the architecture versus manual partitioning under operating-system control, show the range of choices memory management spans.

Source: adapted from "Memory management" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Memory_management

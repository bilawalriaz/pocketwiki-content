# Multithreading (computer architecture)

In computer architecture, multithreading is the ability of a central processing unit (CPU), or a single core in a multi-core processor, to provide multiple threads of execution. A thread here is an independent stream of instructions the processor tracks separately, distinct from a software "thread" managed by an operating system.

The technique became attractive once instruction-level parallelism, the trick of running several instructions from one program at once, hit a wall in the late 1990s. Single programs got harder to speed up, but most systems run many tasks at once, so methods that improve the throughput of all tasks gained importance. Multithreading and multiprocessing, which uses several CPUs or cores, are the two main ways to do this.

## Why it helps

A CPU spends time waiting. A thread that suffers a cache miss, a failed read from the fast on-chip memory that forces a trip to slower off-chip memory, stalls for hundreds of cycles. A thread whose next instruction depends on a result just computed sits idle too. While one thread waits, another can use the parts of the CPU that would otherwise sit empty. The gain comes from filling dead time, not from making any single thread faster.

Intel claims up to 30% improvement with Hyper-Threading Technology. A synthetic loop of dependent floating-point operations, code that leaves the most resources idle, speeds up by about 100% when a second thread is added. Hand-tuned code using MMX or AltiVec SIMD extensions and explicit data prefetching can already keep every resource busy, so it gains nothing and may slow down because caches and TLBs (translation lookaside buffers that cache virtual-to-physical address translations) are now shared with another thread.

Hardware multithreading is also more visible to software than multiprocessing is, so applications and operating systems need more changes. Merging results from two threads can cost orders of magnitude more than processing them in one thread because of inter-process communication and synchronisation.

## Three flavours

The three flavours differ in how often they switch threads and how much hardware they duplicate.

Coarse-grained (block or cooperative) multithreading runs one thread until it stalls, then switches. If thread A misses the cache on cycle *i*+2 while issuing a load, the scheduler swaps in thread B on cycle *i*+3 and issues B's instructions on *i*+4 and *i*+5. To make the swap cheap, the chip duplicates the register set and key control registers such as the program counter, so a switch costs roughly one cycle. This style matches cooperative multitasking in real-time operating systems. Many microcontrollers already use multiple register banks to handle interrupts, which is the same trick between user code and interrupt handlers.

Fine-grained (interleaved) multithreading issues instructions from a different thread every cycle, like a barrel processor rotating through threads the way staves circle a barrel. With only one thread's worth of independent instructions in flight at a time, switching every cycle removes most data-dependency stalls, the same way preemptive multitasking keeps an operating system busy. The price is that every pipeline stage must tag each instruction with its thread ID, and shared resources like caches and TLBs must be larger to avoid thrashing, the constant eviction and reloading caused by too many threads competing for the same storage.

Simultaneous multithreading (SMT) goes furthest on a superscalar processor, one that can issue more than one instruction per cycle. An ordinary superscalar issues several instructions from a single thread each cycle; SMT issues instructions from several threads in the same cycle, so on cycle *i* A's instructions *j* and *j*+1 plus B's instruction *k* can leave the issue stage together. Any one thread has only so much instruction-level parallelism, so SMT fills empty issue slots with work from other threads. The older two styles are grouped as temporal multithreading to contrast with SMT. SMT pays the same tagging and resource costs as fine-grained, more so, because more threads stay active at once.

## Implementation details

The thread scheduler, which picks the next ready thread and tracks stalled ones, can live entirely in hardware, entirely in software, or be split between them. Designers must also decide which events trigger a switch: cache misses, inter-thread communication, DMA completion (a direct-memory-access transfer finishing), and so on.

A final choice is how much state to duplicate. Replicating all software-visible state, including privileged control registers and TLBs, lets each thread run its own operating system as a virtual machine on the same processor. Replicating only user-mode state uses less silicon and leaves room for more threads on the same die area (the slice of silicon occupied by the CPU core), but at the cost of that isolation.

Implementations include DEC's EV8 (never completed), Intel's Hyper-Threading Technology, IBM's POWER5 through POWER9, IBM z13/z14/z15 mainframes, Sun Microsystems' UltraSPARC T2, Cray's XMT, and AMD's Bulldozer and Zen microarchitectures.
```

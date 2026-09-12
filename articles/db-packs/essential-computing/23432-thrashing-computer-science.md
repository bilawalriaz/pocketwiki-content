# Thrashing (computer science)

Thrashing is what happens when a computer spends more time shuffling data between fast and slow memory than doing the work it was asked to do. In paging systems, thrashing appears when real memory (RAM) is overcommitted: too many processes share too little physical memory, so the operating system must constantly move pages (fixed-size blocks, typically 4 KiB) to and from disk, each move generating a page fault (an exception raised when code touches an address whose page is not in RAM).

After a program starts, it touches only a small fraction of its pages at any moment. Those active pages form the working set. A system runs efficiently when the combined working sets fit comfortably inside the page frames (physical slots in RAM that each hold one page) the machine has. As working sets grow, page faults stay manageable until a critical point: faults rise sharply, the time spent resolving them overwhelms computing, and throughput collapses. Recovery usually means closing applications or letting processes finish so virtual memory pressure eases.

The pattern also appears inside a single instruction. On VAX processors, a MOVL with displacement-deferred addressing on both operands, where each operand address crosses a page boundary, references ten pages at once. All ten must be resident before the instruction completes; if any one must be swapped out to make room for another, every retry fails. Pathological locality turns one instruction into a page-fault storm.

The same shape recurs at other levels of the memory hierarchy whenever a fast cache is too small for what the program touches: misses dominate, lookups go slow, performance falls.

## Cache thrashing

A CPU cache is a small, fast memory near the processor holding copies of recently used data from RAM. Cache thrashing happens when accesses compete for the same cache lines, evicting entries that are about to be reused. It appears most with low-associativity caches (where each address can land in only a few slots, called ways), and worsens when hot data is too large or poorly localised. A classic trigger is a strided loop such as `for (k = 0; k < N; k += 256) v[k] += 1`, whose stride matches a power of two and maps many accesses onto the same cache set.

## TLB thrashing

The translation lookaside buffer (TLB) is a small cache inside the memory management unit (MMU, the hardware that translates virtual addresses into physical addresses) that holds recent page translations. Even when code and data fit in the L1 or L2 caches, a working set scattered across many pages can overflow the TLB, turning every memory access into a slow page-table walk. A separate failure is internal collisions inside the TLB's associative memory, where many virtual page numbers hash to the same set. Binary-searching a power-of-two-sized buffer of about 512 KiB or more is a textbook case: lower address bits align, collisions surge, and lookups slow. Spreading the key with an asymmetric midpoint offset such as 31/64 breaks the alignment and restores performance.

## Heap thrashing

When the runtime heap (the pool from which a program allocates objects) is too small or too fragmented, every allocation may trigger a long garbage-collection pause (a stop-the-world sweep that reclaims unused objects) because no large free block can be found. Frequent collection driven by allocation failures is heap thrashing.

## Process thrashing

If cooperating processes cannot all be scheduled together, the running ones keep waking and suspending each other. Each makes a little progress before being preempted, collective throughput collapses, and the system spends more time context-switching than computing.

## Swap-token

A practical defence against system-wide thrashing in Linux is swap-token. A single kernel token is handed to a process that is faulting heavily during a thrashing episode. The holder may allocate extra physical pages to build its working set, finish quickly, and release them. The original scheme used a fixed timestamp; the later preempt swap-token tracks each process's swap-out count and gives the token, with a proportionally longer time slice, to the most memory-pressured process.

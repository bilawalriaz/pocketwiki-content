# External memory algorithm

An external memory algorithm, also called an out-of-core algorithm, processes data too large to fit in a computer's main memory at once. It is designed around the cost of moving data between fast internal memory and slower bulk storage such as a hard drive, a tape, or memory on another machine reachable over a network.

## The external memory model

External memory algorithms are analyzed in the external memory model, also called the I/O model or disk access model. It extends the standard random-access machine model by adding a cache between the processor and an unbounded external store.

The model has two parameters: the cache holds $M$ elements, and both the cache and the external store are partitioned into blocks of $B$ contiguous elements. One I/O transfers one block between external memory and the cache. Running time is the number of such block transfers, not the number of individual element accesses.

Two facts drive algorithm design in this model. Cache accesses are much cheaper than external accesses, and reading a whole block of $B$ elements is cheaper per element than reading $B$ scattered single elements, because sequential access avoids seeking with a disk head. Reusing data once it has been fetched into the cache, so a single block transfer serves many operations, is called locality.

The model was introduced by Alok Aggarwal and Jeffrey Vitter in 1988. It is related to the cache-oblivious model, but cache-aware algorithms may use the known values of $M$ and $B$, while cache-oblivious algorithms must work for any $M$ and $B$.

## Searching: B-trees

Searching for one element among $N$ stored items, and inserting or deleting items, can be done with a B-tree whose branching factor is $B$. Each tree level corresponds to one block transfer, so search, insert, and delete run in $O(\log_B N)$ I/Os. This matches the information-theoretic lower bound for the problem, so B-trees are asymptotically optimal.

## Sorting

External sorting sorts $N$ items that do not fit in cache. Two standard approaches both reach the asymptotically optimal $O\!\left(\tfrac{N}{B}\log_{\tfrac{M}{B}} \tfrac{N}{B}\right)$ I/Os: a $k$-way merge sort with $k = M/B$ runs, and a distribution sort patterned on quicksort that partitions items into $M/B$ buckets in one pass. The same bound governs the fast Fourier transform in this model.

## Permutation

The permutation problem rearranges $N$ elements into a given order. It can be solved by sorting, which takes the external sort bound above, or by inserting each element into its target position and ignoring locality, which takes $O(N)$ I/Os. The combined cost is $O\!\left(\min\!\left(N,\ \tfrac{N}{B}\log_{\tfrac{M}{B}} \tfrac{N}{B}\right)\right)$, matching the lower bound.

## Applications

The model captures the memory hierarchy, the layered structure of caches, RAM, and disk, that simpler random-access models ignore, and it is the standard tool for proving lower bounds on data structures whose performance depends on that hierarchy. It is used wherever datasets exceed internal memory, including geographic information systems and digital elevation models that reach gigabytes or terabytes, and it extends beyond CPUs to GPU computing, where transfer between CPU and GPU memory is the bottleneck, and to classical digital signal processing.

## History

The adjective out-of-core predates the algorithm literature. It appears in 1962 describing devices outside the core memory of an IBM 360, and in 1971 in reference to algorithms.

Source: adapted from "External memory algorithm" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/External_memory_algorithm

# Basic Linear Algebra Subprograms

Basic Linear Algebra Subprograms (BLAS) is a specification for low-level routines that perform the small, repeated operations underlying numerical linear algebra: vector addition, scalar multiplication, dot products, linear combinations, and matrix multiplication. The spec is language-agnostic, with standard bindings for C (CBLAS) and Fortran (BLAS). Most linear-algebra libraries conform to it, so programs can swap implementations without code changes.

The spec is fixed, but real implementations are tuned to the host hardware, exploiting vector registers, SIMD instructions, and the cache hierarchy. LINPACK, LAPACK, MATLAB, NumPy, Julia, R, Mathematica, GNU Octave, Armadillo, and the C++26 `std::linalg` library all rely on a BLAS implementation for their core linear-algebra operations.

## Origin and three-level structure

BLAS began as a Fortran library published in September 1979 by Lawson, Hanson, Kincaid, and Krogh. It packaged a set of "kernel" operations identified between 1973 and 1977, replacing the ad-hoc nested loops then in common use. LINPACK was the first major consumer.

As machines evolved, the kernel set grew and was grouped by complexity into three levels:

- **Level 1** (1979): vector–vector operations on strided arrays, meaning arrays whose elements are evenly spaced in memory. The defining routine is `axpy`, y ← αx + y, which scales one vector and adds it to another.
- **Level 2** (1984–1988): matrix–vector operations. The workhorse is `gemv`, y ← αAx + βy, plus a solver for triangular systems. These expose matrix–vector structure to vector machines, where Level 1 code hides it from the compiler.
- **Level 3** (1990): matrix–matrix operations, built around `gemm`, C ← αAB + βC. A and B can optionally be transposed or Hermitian-conjugated inside the routine, and all three matrices may be strided.

The level numbers match the polynomial degree of the operations: O(n) for Level 1, O(n²) for Level 2, O(n³) for Level 3. Higher levels do more arithmetic per byte of data moved, which is why Level 3 is the primary optimization target on cache-based CPUs.

## Why Level 3 matters

`gemm` is the heart of BLAS. Block-partitioned algorithms (splitting matrices into smaller sub-matrices) require the β parameter, which lets the routine accumulate partial results into an existing C; the β = 1 case is special-cased to save a multiplication per element. Block sizes are chosen to match cache lines, keeping data in fast memory, and a second round of blocking targets multi-level cache hierarchies. Kazushige Goto showed that careful L2-cache blocking plus reduced TLB misses (misses in the Translation Lookaside Buffer, the hardware that translates virtual to physical addresses) can beat earlier auto-tuning systems like ATLAS. His ideas live on in GotoBLAS, OpenBLAS, and BLIS.

A common variant is `gemm3m`, which multiplies two complex matrices using three real multiplications and five real additions instead of the usual four and two, a technique resembling Strassen's algorithm and first described by Peter Ungar.

## Implementations

The Netlib reference implementation, written in Fortran 77 and in the public domain, is correct but unoptimized and is used mainly as a baseline. Most users pick a tuned library:

- **OpenBLAS**, an open-source, hand-optimized fork of GotoBLAS supporting x86, x86-64, MIPS, ARM, and RISC-V.
- **BLIS**, a framework and a refactoring of GotoBLAS that reduces the per-architecture code required.
- **ATLAS**, which auto-tunes itself at install time to whatever CPU it finds.
- **Intel MKL**, free for some uses and proprietary for others, tuned for x86/x86-64 with strong performance on Intel CPUs.
- **Arm Performance Libraries**, tuned for AArch64.
- **Accelerate**, Apple's framework shipping tuned BLAS and LAPACK on macOS and iOS.
- **cuBLAS** (NVIDIA) and **rocBLAS** (AMD) for GPUs.

## Extensions

The original spec covers only dense vectors and matrices. Two extensions have since been standardized:

- **Sparse BLAS**, a small kernel set for sparse matrices, standardized in 2002.
- **Batched BLAS**, specified in 2017 for parallel hardware such as GPUs. The traditional GEMM performs poorly on stacks of many small matrices because per-call overhead dominates. Batched GEMM applies C[k] ← αA[k]B[k] + βC[k] to every matrix k in a stack at once, often in a strided layout. Time-stepping integrators such as exponential or Magnus integrators use it to parallelize the expensive matrix exponential across time steps.

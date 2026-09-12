# Programming with Big Data in R

pbdR is a suite of R packages for statistical computing on big data, first released in September 2012 by Wei-Chen Chen, George Ostrouchov, Pragneshkumar Patel, and Drew Schmidt. The pbdR Core Team maintains it; the source lives on GitHub at RBigData. It is dual-licensed under the GPL and the Mozilla Public License and is influenced by R, C, Fortran, MPI, and ØMQ.

The defining contrast with ordinary R is the target machine. Base R runs on a single multi-core machine driven interactively through a GUI. pbdR targets distributed-memory systems, where a large dataset is partitioned across many processors that exchange messages through MPI, the standard Message Passing Interface used in high-performance computing (HPC) clusters. Two MPI-backed implementations exist for R: Rmpi and pbdR's own pbdMPI.

## Parallel styles

Two parallel styles sit behind these implementations.

SPMD (Single Program, Multiple Data), introduced in the mid-1980s, runs the same code on every processor, each working on its own slice of the data. It is most efficient on homogeneous clusters and suits batch workloads such as singular value decomposition (SVD) on a large matrix or clustering on high-dimensional data. A modern GPU follows the same idea: many slow co-processors apply one kernel to different data partitions, shortening time-to-solution.

Manager/workers parallelism, the style Rmpi uses, emerged around 2000. One manager process dispatches tasks to workers. It suits small clusters running embarrassingly parallel statistical jobs such as bootstrap resampling or Monte Carlo simulation, both of which rely on the i.i.d. (independent and identically distributed) assumption. Task-pull variants perform better in heterogeneous clusters. SPMD code can also adopt a manager/workers pattern, so the two styles are not mutually exclusive.

## Package design

pbdR is a stack, not a single library. pbdMPI sits at the base, wrapping OpenMPI or MPICH2 and producing the shared library and configuration file that every other package links against. That configuration step removes the usual pain of compiling against MPI. Built on top are:

| Layer | Packages |
|---|---|
| Distributed data and linear algebra | pbdBASE, pbdDMAT, pbdSLAP, kazaam |
| I/O | pbdNCDF4 (Parallel NetCDF 4), pbdADIOS |
| Computation and applications | pmclust (parallel model-based clustering), pbdML, pbdDEMO |
| Profiling | pbdPROF, pbdPAPI, hpcvis |
| Client/server | pbdZMQ (ØMQ interface), remoter, pbdCS, pbdRPC |

pbdSLAP bundles ScaLAPACK 2.0.2 along with BLACS and PBLAS for double-precision dense linear algebra. pbdDMAT supplies the distributed matrix classes that applications use. pbdDEMO ships more than twenty runnable examples and a vignette that walks through the maths and statistics behind them.

## Running pbdR code

Because every processor executes the same script, pbdR programs are written to a file and launched from the command line with mpiexec or mpirun, the standard MPI process launchers. They are not typed into an interactive R session.

A minimal pbdMPI program initialises MPI, performs a collective operation, and finalises:

```
library(pbdMPI, quiet = TRUE)
init()
comm.cat("Hello World!\n")
finalize()
```

Saved as `demo.r`, the command `mpiexec -np 2 Rscript demo.r` runs the script on two processors.

A second example shows SPMD data distribution. With `N <- 5`, each rank `r` sets `x <- (1:N) + N * .comm.rank`, so processor 0 holds 1–5, processor 1 holds 6–10, and so on. Calling `allreduce(x, op = "sum")` sums across ranks; the source runs the call twice, with integers and doubles, to show the type-preserving variants.

A third example, drawn from pbdDEMO, distributes a 16×16 matrix of `rnorm` values (mean 100, sd 10) across a 2×1 process grid using `ddmatrix`, computes its SVD with `La.svd`, and prints the singular values to confirm the result is consistent across ranks.

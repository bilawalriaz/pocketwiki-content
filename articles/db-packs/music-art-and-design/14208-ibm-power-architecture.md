# IBM POWER architecture

IBM POWER is a RISC (reduced instruction set computer) instruction set architecture (ISA) developed by IBM. The name is an acronym for Performance Optimization With Enhanced RISC. Introduced in 1990, it powered high-end IBM microprocessors in servers, workstations, minicomputers, and supercomputers, then evolved into PowerPC (1992) and Power ISA (2006).

## The 801 and Cheetah

POWER descends from IBM's 801 research project at the Thomas J. Watson Research Center. Started in 1974 to build a telephone switch estimated at 12 MIPS, the project needed only simple operations: I/O, branches, register-register add, and register-memory moves. From this minimal instruction set came the RISC design rule that every instruction completes in one fixed clock cycle, with no micro-decoded complex operations. The telephone project was cancelled in 1975 without a prototype, but the 801 design continued as a general-purpose CPU.

By 1982, the Cheetah project tested whether a RISC design could issue more than one instruction per cycle, the superscalar approach. Cheetah added separate branch, fixed-point, and floating-point execution units. By 1984 the team migrated from bipolar ECL to CMOS to gain integration density.

## America project and the first POWER chip

In 1985, a second-generation RISC effort at Watson produced the "AMERICA architecture," and in 1986 IBM Austin used it to design the RS/6000 product line. The first RS/6000 systems shipped in February 1990 as POWERstation and POWERserver models, running the POWER1 CPU. RIOS-1, the high-end configuration, spread the chip across 10 discrete dies: instruction cache, fixed-point, floating-point, four data cache, storage control, I/O, and clock chips. A lower-cost RIOS.9 used 8 chips; a single-die RSC (RISC Single Chip) followed in 1992.

America fixed two 801 limitations. The 801's single-cycle rule excluded floating-point, and although its decoder was pipelined, it did not exploit superscalar dispatch. America added a dedicated FPU and a decoder that could fetch, decode, and dispatch an instruction to the ALU and FPU simultaneously, making POWER one of the first commercial superscalar CPUs. The architecture exposed 32 32-bit integer registers and 32 64-bit floating-point registers, plus branch-unit private registers including the program counter. Applications saw a 52-bit virtual address space, letting programs share a flat 32-bit region while partitioning memory separately.

## POWER2 and P2SC

POWER2, announced in November 1993, added a second fixed-point unit and a second floating-point unit, gaining leadership performance at launch. New instructions included quad-word loads, hardware square root, and floating-point-to-integer conversion.

In 1996, IBM produced P2SC, a single-die POWER2 in its CMOS-6S process. At introduction it was the largest, highest transistor-count processor in the industry, and it powered the 1997 Deep Blue supercomputer that defeated Garry Kasparov.

## Transition to PowerPC and Power ISA

The original POWER ISA was deprecated in 1998 when POWER3 arrived. POWER3 was primarily a 32/64-bit PowerPC processor that retained POWER features for backward compatibility. PowerPC evolved into Power ISA in 2006. IBM continues to develop PowerPC cores for embedded ASICs, and the lineage runs through today's Power10 processors used in servers, with PowerPC cores embedded in NXP, Nintendo, and aerospace designs.

| Generation | Year | Key trait |
|---|---|---|
| 801 | 1975 | RISC with fixed-cycle instructions |
| Cheetah | 1982 | Superscalar exploration |
| POWER1 | 1990 | First chip; multi-chip RIOS |
| POWER2 / P2SC | 1993 / 1996 | Dual fixed/float units; single-die P2SC |
| POWER3 | 1998 | Transition to 32/64-bit PowerPC |
| PowerPC → Power ISA | 2006 | Modern lineage through Power10 |

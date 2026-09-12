# MIPS architecture

MIPS (Microprocessor without Interlocked Pipelined Stages) is a family of RISC instruction set architectures (ISAs) developed by MIPS Computer Systems, now MIPS Technologies, and introduced in 1985. It is a load–store ISA: only dedicated load and store instructions touch memory, while arithmetic, logical, and control-flow instructions operate on registers. Fixed-length 32-bit instructions keep decoding simple, and 32 general-purpose registers plus 32 floating-point registers give compilers enough space to keep operands in registers. Bi-endian byte order and 4 KB pages are part of the base specification. The current standard is MIPS32/64 Release 6 (2014).

The architecture has shaped how computer-architecture courses teach pipelines and ISAs, and it influenced later RISC designs such as Alpha. In March 2021 Wave Computing ended MIPS development in favour of RISC-V.

## Versions

Each version up through MIPS V was a strict superset of the previous one. In 1999 MIPS32 and MIPS64 split the line into parallel 32-bit and 64-bit specifications; the 64-bit line is based on MIPS V and adds a 32-bit compatibility mode.

| Version | Year | Key change |
|---|---|---|
| MIPS I | 1985 | 32 GPRs, HI/LO for multiply–divide, branch and load delay slots |
| MIPS II | 1989 | Removed load delay slot; added LL/SC atomics, branch-likely, trap-if-conditional |
| MIPS III | 1991 | 64-bit GPRs, addresses, and integer operations; supervisor mode |
| MIPS IV | 1994 | Indexed FP addressing, prefetch, conditional moves, FP multiply–add |
| MIPS V | 1996 | Paired-single SIMD in FP registers; no silicon shipped; folded into MIPS64 |
| MIPS32/64 R6 | 2014 | Removed delay slots, reorganised encoding, PC-relative addressing |

## Instruction encoding

Every MIPS instruction is 32 bits long and begins with a 6-bit opcode; the remaining fields depend on the format:

| Type | Fields |
|---|---|
| R (register) | opcode, rs, rt, rd, shamt, funct |
| I (immediate) | opcode, rs, rt, 16-bit immediate |
| J (jump) | opcode, 26-bit address |

The single addressing mode is base register plus a sign-extended 16-bit displacement. Loads and stores handle bytes, halfwords, and words; sub-word loads are sign-extended by default and zero-extended only with the "unsigned" suffix. Misaligned accesses raise an exception unless load/store-left/right instructions are used.

## Delay slots, branches, and coprocessors

Early MIPS used a branch delay slot (the instruction after a branch always executed) and a load delay slot (the instruction after a load could not read the loaded value). Compilers or assemblers filled these slots with useful work or with NOPs. Release 6 removed both delay slots and added new branch-and-link forms with PC-relative offsets.

The architecture reserves up to four coprocessor slots. COP0 is the system-control coprocessor used by the kernel, COP1 is the optional floating-point unit, and COP2/COP3 are implementation-defined. The original PlayStation used COP2 for its Geometry Transformation Engine; MIPS III deleted COP3 and reused its opcodes for 64-bit operations.

## Extensions

Optional application-specific extensions add capabilities without changing the base ISA. MIPS-3D adds 13 instructions for 3D geometry. MDMX provides integer SIMD that reuses the FP registers. MIPS16e and its successor microMIPS compress common instructions to 16 bits, shrinking program size by up to 40%. MIPS MT adds hardware multithreading through virtual processing elements. The DSP extension adds saturating and fixed-point arithmetic, and MIPS MSA defines a 128-bit SIMD instruction set. SmartMIPS targets smart cards.

## Calling conventions

The 32-bit O32 ABI passes arguments in $a0–$a3 and returns values in $v0. The 64-bit N64 ABI (and N32, its 32-bit-pointer variant) pass eight arguments in $a0–$a7 and treat every register as 64 bits wide. In all variants the callee must preserve $s0–$s7, $gp, $sp, and $fp; $k0 and $k1 are reserved for the kernel and can be overwritten at any interrupt.

## Applications and decline

Through the 1990s MIPS powered SGI and NEC workstations and servers, the Nintendo 64, PlayStation, PlayStation 2, and PlayStation Portable. After MIPS Technologies was spun out of SGI in 1998, the market shifted to embedded systems: residential gateways, routers, automotive controllers, and LTE modems. Wave Computing opened the ISA in December 2018, made Release 6 royalty-free in March 2019, then shut the open programme down later that year. Loongson continues to extend MIPS-compatible ISAs and won a rights case over the architecture in January 2024.

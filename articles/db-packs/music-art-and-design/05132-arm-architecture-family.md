# ARM architecture family

ARM is a family of RISC instruction set architectures for processors. Arm Holdings designs the ISA and licenses it to other companies, who build the physical chips. The same company also sells pre-designed processor cores that implement the ISA. This dual model is the key to ARM's spread: licensees can buy a ready-made core for cheap integration, or design their own against the ISA with full freedom to optimise for speed, power, or added instructions.

Low cost, low power draw, and low heat have made ARM the default choice for smartphones, tablets, laptops, embedded devices, and single-board computers like the Raspberry Pi. The same chips also power desktops, servers, and supercomputers; Japan's Fugaku was the world's fastest supercomputer from 2020 to 2022 using ARM. Over 230 billion ARM chips have shipped since at least 2003.

## Origins at Acorn

ARM began at Acorn Computers in the early 1980s after Acorn judged the available 16-bit and 32-bit CPUs too expensive and barely faster than their own BBC Micro design. Berkeley RISC research showed a simple chip could outperform complex 32-bit designs, and a visit to the Western Design Center, where high school students were laying out chips on Apple IIs, convinced engineers they could build their own. Acorn's Sophie Wilson and Steve Furber started the project in October 1983. Wilson wrote the instruction set in BBC BASIC, and VLSI Technology fabricated the silicon. ARM1 worked on first power-up in April 1985 at 6 MHz. ARM2 followed in late 1986 at 8 MHz, adding a hardware Booth multiplier and a Fast Interrupt (FIQ) mode that banks extra registers so interrupt handlers save fewer registers.

Two original design choices had lasting impact. First, the program counter and processor flags shared one 32-bit register, so an interrupt could save the full machine state in a single store. Second, special S-cycle instructions exploited page mode DRAM, where sequential accesses to the same memory page run at double speed, roughly doubling memory bandwidth for graphics and I/O. The trade-off was a 26-bit address space, capping memory at 64 MB.

## Architecture evolution

ARMv3 removed the 26-bit cap and introduced a full 32-bit address space. ARM stayed 32-bit through ARMv7. In 2011, ARMv8-A added 64-bit support through a new execution state called AArch64, with the A64 instruction set and 32 general-purpose 64-bit registers. Processors can run in either 32-bit (AArch32) or 64-bit (AArch64) mode. Armv9-A, announced in 2021, keeps the 64-bit base but emphasises security.

ARMv7 defined three profiles: A (Application, Cortex-A), R (Real-time, Cortex-R), and M (Microcontroller, Cortex-M). ARMv6-M is a stripped subset of ARMv7-M for the smallest chips. Optional extensions are the main reason for ARM's flexibility. Thumb (1994) adds 16-bit compressed instructions for better code density; Thumb-2 mixes 16- and 32-bit forms. Jazelle (1999) added Java bytecode execution and is now deprecated. NEON provides 64/128-bit SIMD for audio, video, and signal processing. VFP adds floating-point, with later versions including half-precision. TrustZone splits execution into a Secure world and a Normal world on the same core, used for DRM, key storage, and trusted boot; the Armv8-M variant uses branch-based world switching for low-latency calls. Helium (MVE, 2019) adds vector extensions for Cortex-M microcontrollers.

## Core ideas of the instruction set

The 32-bit ISA is a RISC load-store design where only load and store instructions touch memory and arithmetic works on registers. There are 16 visible 32-bit registers, including the program counter (R15), stack pointer (R13), and link register (R14). Most instructions are 32 bits and execute in a single cycle. A barrel shifter folds shifts and rotates into arithmetic for free.

Three features are unusual for RISC. Conditional execution (predication) lets nearly every instruction carry a 4-bit condition code and be skipped when false, removing many short branches. Fast interrupts bank R8-R14 in FIQ mode, so handlers save fewer registers. PC-relative addressing treats the program counter as a general register, simplifying position-independent code. Pipelines grew with demand: ARM7 had three stages, Cortex-A8 has thirteen.

## Licensing model

Arm Holdings sells designs, not chips. A licensee combines an ARM core with its own peripherals and memory controllers to produce a system-on-chip (SoC), then fabricates it at a foundry. A core licence delivers a ready-made core, either a hardened layout or synthesizable RTL; hundreds of millions of ARM7TDMI cores shipped this way. A Built on Cortex licence (2016) lets licensees modify a Cortex design privately, used by Qualcomm's Kryo 280. An architectural licence lets licensees design their own core against the ISA, used by Apple, Qualcomm, Samsung, and Nvidia. Arm Flexible Access (2019) offers unlimited pre-production access to most ARM IP, with per-product fees due at tape-out.

## Debugging, security, and software

Modern cores include hardware debug via JTAG or ARM's two-wire SWD protocol, supporting breakpoints, watchpoints, and halt or monitor mode debugging. ARMv6 added execute-never page protection. The Large Physical Address Extension (LPAE, 2011) widened physical addresses to 40 bits. The PSA Certified security scheme (introduced 2017) provides a standard framework for securing IoT devices built on ARM.

Operating system support is broad. Android supports Armv8-A since version 5.0; iOS since iOS 7 and 64-bit-only since iOS 11; Linux since kernel 3.7 in late 2012; Windows 10 and 11 run native ARM64 plus emulated x86; macOS has run on Apple silicon since Big Sur in late 2020. Embedded RTOSs including FreeRTOS, QNX, VxWorks, Zephyr, and seL4 all support ARM.

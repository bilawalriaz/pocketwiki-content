# Asynchronous circuit

An asynchronous (clockless or self-timed) circuit is a sequential digital circuit with no global clock coordinating its components. Blocks signal completion to one another through a handshaking protocol, so the circuit advances whenever inputs are ready and work is done.

## Why synchronous circuits use a clock

Digital logic splits into combinational logic (outputs depend only on current inputs) and sequential logic (outputs depend on current and past inputs, because the circuit contains memory). Sequential logic needs a way to say "now is the moment to read and update the state."

Synchronous circuits use an electronic oscillator that emits a regular train of clock pulses. Every flip-flop changes only on a clock edge, so the entire circuit steps forward in lockstep. The time a signal takes to travel through a chain of combinational gates is its propagation delay, and the longest chain (the critical path) sets the maximum safe clock rate; faster paths idle while waiting for the slowest.

Clocked ICs pay several costs. Engineers must verify that the clock reaches every part of the chip nearly simultaneously, or timing fails; when it does not, the error is called clock skew. The clock distribution network burns significant power and runs continuously, even when the circuit is idle. Timing verification consumes more than half of synchronous design effort, and the global clock's tight fan-out and harmonics generate concentrated electromagnetic interference (EMI).

## How asynchronous circuits differ

An asynchronous circuit changes state as soon as its inputs change; there is no global tick. Local functional blocks remain usable, but the clock skew problem is gone. Speed is bounded by local propagation delays rather than the chip's worst-case critical path.

The trade-off is sensitivity to race conditions. If two inputs reach a gate almost simultaneously, small differences in gate delay can drive the circuit into the wrong state. In synchronous designs this risk is mostly contained because internal transitions align to the clock; in asynchronous designs, the relative arrival times of signals matter everywhere. This makes asynchronous logic harder to design, test, and debug, and the surrounding design automation toolchain has historically been weaker.

## Theoretical foundations

The formal theory of asynchronous circuits was created by David E. Muller in the mid-1950s and presented in Raymond Miller's *Switching Theory*. Design styles are placed on a spectrum of delay assumptions. The bundled-delay model uses conventional data paths with a locally generated delay to indicate completion. Delay-insensitive designs, in their purest form quasi-delay-insensitive (QDI), tolerate arbitrary gate and wire delays and are "correct by design," at the cost of larger circuits. Karl M. Fant's 2005 *Logically Determined Design* uses four-valued logic (adding null and intermediate to true and false), a well-known QDI approach; Scott C. Smith and Jia Di extended it into Multi-threshold Null Convention Logic (MTNCL), also called Sleep Convention Logic, for ultra-low-power operation.

Petri nets, particularly Signal Transition Graphs (STGs) introduced in 1985 by Leonid Rosenblum, Alex Yakovlev, and independently Tam-Anh Chu, became the standard formalism for asynchronous control. Tools such as Petrify and Workcraft are widely used for analysis and synthesis.

## Benefits

Average-case performance replaces worst-case: a fast operation completes in its actual time, not the time dictated by the slowest possible case, and speculative completion has produced asynchronous adders faster than synchronous ones. Pipelines are elastic, accepting variable input rates without rigid timing. With no global clock, power is consumed only on demand, with effectively zero standby power; Epson reported 70% lower power than a comparable synchronous design in 2005. Speed tracks temperature and voltage, and current draw spreads in time rather than concentrating at clock edges, reducing EMI and voltage spikes. The circuits tolerate transistor-to-transistor variation, voltage changes, and fabrication drift.

## Costs and limits

Handshaking logic adds area, and an asynchronous design can require up to roughly twice the resources of a synchronous one. Designers manage metastability in arbiters explicitly. Tool support has long lagged the synchronous EDA ecosystem, though the gap narrowed by 2006. Few engineers were trained in asynchronous design in the 1990s and 2000s, and synchronous techniques such as clock gating approximate many of its benefits at lower complexity.

## Communication: protocols and encodings

In a two-phase handshake (non-return-to-zero), any wire transition, rising or falling, counts as an event. In a four-phase handshake (return-to-zero), a data transition is followed by a reset. Four-phase is often faster and simpler because wires end each exchange in a known state; two-phase requires the circuit to remember polarity internally.

Bundled-data encoding carries each data bit on one wire alongside separate request and acknowledge wires, with the receiver assuming a bounded data delay. This is the same encoding used in synchronous design minus the clock, and such circuits are often called micropipelines. Multi-rail encoding uses several wires to encode a value: one-hot (1-of-n) places the digit on one of n wires, and dual-rail uses a pair per bit (one wire for 0, one for 1), making the encoding delay-insensitive because data and request are the same event. With a four-phase protocol, dual-rail is also called three-state encoding, since each pair sits in one of two valid states (01 or 10) or the reset state 00.

## Asynchronous CPUs and history

A clockless CPU coordinates pipeline stages with local pipeline controls or FIFO sequencers: the next stage starts when the previous stage signals completion, so stages run at different speeds and finish early when data permits, for instance when multiplying by 0 or 1. Most commercial CPU tools assume a clocked style and must be modified, and metastability is managed by hand; the AMULET group at Manchester built a custom tool called LARD for this reason.

The first asynchronous computer was the ORDVAC in 1951. Caltech's Asynchronous Microprocessor (CAM, 1988) was the first asynchronous microprocessor, a 16-bit QDI RISC fabricated in gallium arsenide reaching about 100 MIPS; in demonstrations its instruction rate slowed when the chip was heated and rose under liquid nitrogen cooling, with no reconfiguration. Caltech followed with MiniMIPS in 1998 (32-bit MIPS I, predicted around 280 MIPS at 3.3 V, measured roughly 40% lower due to layout mistakes) and the Lutonium 8051 in 2003. Other notable designs include the AMULET ARM processors (1993, 2000), Epson's ACT11 flexible 8-bit chip (2004), Intel's Vortex superscalar test chip (2007), Charles H. Moore's SEAforth (2008) and GA144 (2010) multi-core chips, Handshake Solutions' ARM996HS (2006) and HT80C51, the SAMIPS asynchronous MIPS R3000, and IBM's 2014 SyNAPSE chip, one of the highest transistor-count chips ever produced, which runs asynchronously and consumes orders of magnitude less power than conventional systems on pattern-recognition benchmarks.

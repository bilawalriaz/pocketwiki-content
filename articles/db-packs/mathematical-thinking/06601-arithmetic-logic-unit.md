# Arithmetic logic unit

An arithmetic logic unit (ALU) is the combinational digital circuit inside a processor that performs arithmetic and bitwise operations on integer binary numbers. It is a fundamental building block of CPUs, graphics processing units (GPUs), and floating-point units (FPUs), although FPUs are dedicated to floating-point numbers. Because the ALU is purely combinational, its outputs change asynchronously whenever its inputs change, with a short propagation delay before the result settles.

## Inputs and outputs

A typical ALU has three parallel data buses: two operand inputs, A and B, and a result output, Y. The bus widths usually match the native word size of the surrounding processor, so an 8-bit processor has 8-bit ALU buses. The opcode input is a parallel bus of bits that selects which operation the ALU performs; the number of distinct operations is limited by the opcode width, so a 4-bit opcode can specify up to sixteen operations. The opcode is generally not the same as a full machine instruction, although it may be encoded as a bit field inside one.

Status outputs are individual signals conveying extra information about the most recent result. Common ones are:

| Signal | Meaning |
|---|---|
| Carry-out | Carry from addition, borrow from subtraction, or overflow bit from a shift |
| Zero | All bits of Y are 0 |
| Negative | Arithmetic result is negative |
| Overflow | Arithmetic result exceeded the numeric range of Y |
| Parity | Even or odd number of 1-bits in Y |

A status input, usually a single carry-in bit, lets the ALU receive a carry stored from a previous operation, which is the mechanism that lets ALUs chain together for wider arithmetic.

## How an ALU is used

A CPU drives an ALU by holding its inputs stable, waiting past the propagation delay, and then sampling the output. Sequential logic paces this with a clock slow enough to guarantee the result has settled under worst-case conditions. For an addition, the CPU routes two operands to A and B, sets the opcode to add, enables a destination register, waits for the next clock, and on that clock edge the register latches the sum.

## Operations

A general-purpose ALU supports a standard repertoire.

Arithmetic: add, add with carry, subtract, subtract with borrow, two's complement negation, increment, and decrement. In subtraction the carry-out line reports a borrow, and the operation can be used purely to compare magnitudes, with only the status bits consumed.

Bitwise logic: AND, OR, exclusive-OR (XOR), and ones' complement. AND is also used to test selected bits, where the data result is discarded and only the status bits, especially zero and negative, are kept.

Bit shifts: arithmetic shift preserves the sign bit and applies to two's complement integers; logical shift shifts in a 0 and applies to unsigned integers; rotate wraps bits end-to-end as a circular buffer; rotate through carry treats the carry bit and operand together as a longer circular buffer. Simple ALUs shift by one bit per operation; more capable ones use a barrel shifter to shift by any number of bits in one step. The bit shifted out always appears on carry-out, while the bit shifted in depends on the shift type.

A pass-through operation, in which A is copied unchanged to Y, exists mainly so the CPU can test or copy an operand.

## Status usage and multiple-precision arithmetic

Status outputs are normally stored in an external status register, also called a condition code register, after each operation. Individual bits may or may not be updated depending on the operation; the carry bit is typically left unchanged by AND and OR because it is not relevant. In CPUs the stored carry-out is wired back to the ALU's carry-in input so carries chain from one operation to the next without software intervention.

This carry chain is what makes multiple-precision arithmetic work. To add numbers larger than the ALU's word size, operands are split into fragments matching the ALU word size. The algorithm starts with the least-significant fragments, producing a partial result and a carry-out that is stored. The next fragments are then added along with that stored carry-in, producing the next partial, and the process repeats until every fragment has been processed. The stored carry-out from one step is the carry-in to the next, automatically propagating carries across the whole wide number.

For left shifts, fragments are processed least-significant first so the bit shifted out of each partial, carried over, becomes the least-significant bit of the next. Right shifts are processed most-significant first for the analogous reason. Bitwise operations have no inter-fragment dependency, so the fragment order is irrelevant.

## Data paths and complex operations

ALU operands and results are routed through multiplexers connected to a register file, an accumulator, memory, or an immediate value encoded in the instruction. Because making the ALU perform complex functions directly would inflate circuit size, power, delay, and cost, complex operations are normally broken into sequences of simple ALU steps orchestrated by software. Architectures that need more speed use multiple ALUs in a pipeline, with intermediate results passing from one ALU to the next like a production line, or, in GPUs, hundreds or thousands of ALUs running in parallel, as when many ALUs each process one pixel in a scene.

## Implementation and history

ALUs have been built as mechanical, electromechanical, and electronic circuits. Electronic ALUs appeared as stand-alone integrated circuits in 1967 with the Fairchild 3800, an eight-bit arithmetic unit with accumulator that supported add and subtract but no logic functions. Four-bit bit-slice ALUs such as the Am2901 and 74181 followed; they exposed carry-lookahead signals so several chips could combine into a wider ALU and were widely used in bit-slice minicomputers. When microprocessors arrived in the early 1970s, die space was still tight, so some, including the Zilog Z80, used a narrower ALU than their external word size and needed multiple clock cycles per instruction. The Z80 performed eight-bit additions with a four-bit ALU. Mathematician John von Neumann proposed the ALU concept in 1945 in a report on the EDVAC, and the 1951 Whirlwind I was the first computer to use multiple parallel single-bit ALU circuits, sixteen of them, to operate on 16-bit words. As transistor geometries shrank, full-width ALUs became standard, and modern ALUs commonly include barrel shifters and binary multipliers so operations needing many cycles on older hardware complete in a single cycle.

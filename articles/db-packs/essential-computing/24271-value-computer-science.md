# Value (computer science)

In computer science, a **value** is the representation of some entity that a program can manipulate. The members of a type are the values of that type, so every value carries a type that fixes what operations are valid on it. The "value of a variable" is whatever the current environment mapping returns for that variable's name.

In declarative, high-level languages, values must be referentially transparent: the result of an expression depends only on the contents of its operands (the bits and their interpretation), not on the memory location of the expression. In languages with assignable variables, a single name must distinguish between location and contents.

## l-values and r-values

The l-value/r-value split, introduced by Combined Programming Language (CPL), captures that distinction. The names come from the left and right sides of an assignment.

- An **l-value** names an object that persists beyond a single expression and has a storage location the program can reach, for example a named variable `x` or a dereferenced pointer.
- An **r-value** is a temporary that exists only while the expression that produces it is being evaluated. In `4 + 9` the computer produces13, but no named slot holds it, so the result is a non-l-value (an r-value that is not an l-value).

A variable carries both halves. After `int x = 13;`, the name `x` denotes a location (l-value) whose current contents are 13 (r-value).

The split maps loosely onto parameter modes: input parameters are r-values, output parameters are assignable l-values, and input/output parameters are l-values that can be both read and written. Technical details differ across languages, but the underlying distinction (has a value versus can be assigned to) is the same.

## Refinements

In early C, l-value meant "something assignable." Once `const` was added, the term shifted to **modifiable l-value**, because a `const int` has an address but cannot be written through.

C++11 complicated the taxonomy to support move semantics. The reference notation `&&` binds a compiler-only handle to an expression's address; the address is not retrievable at run time with `&`. Objects near the end of their lifetime, whose resources can be reused cheaply, are **x-values** (expiring values). C++ now uses three categories: **gl-value** (generalized l-value, covering l-values and x-values), **pr-value** (pure r-value, an r-value that is not an x-value), and the legacy l-value and r-value labels as special cases.

## Immediate values in machine instructions

A value does not need to live in memory. Most instruction sets include one or more **immediate** operands, sometimes labelled "imm." An immediate is encoded directly inside the machine instruction that uses it, alongside the opcode and the destination register (the destination may be implicit).

Processors usually support several immediate widths (8-bit, 16-bit, and so on), each with its own opcode and mnemonic; a literal that does not fit triggers an "Out of range" assembler error. Most assemblers accept the same literal written as ASCII, decimal, hexadecimal, octal, or binary, so `'A'`, `65`, and `0x41` denote the same byte. Multi-byte strings follow a byte order that depends on the processor and assembler.

A non-immediate operand sits in a register or elsewhere in memory, and the instruction must carry a direct or indirect address (for example, an index-register address) pointing to it. Immediate and addressed operands are the two ways a value physically reaches an executing instruction, and the choice changes both instruction size and how a value can be reused across statements.

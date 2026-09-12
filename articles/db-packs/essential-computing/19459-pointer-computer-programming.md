# Pointer (computer programming)

A pointer is a variable that stores the memory address of another value rather than the value itself. Reading the data at that address is called dereferencing. A page number in a book's index is a pointer to a page; flipping to that page dereferences it.

Because indirection is fundamental to algorithms, most languages expose pointers as a core feature. In statically typed languages the pointer type includes the type of datum pointed to, so `int *` and `char *` are distinct types even though both hold addresses.

## Hardware roots

Most architectures assign each byte a numeric address, turning memory into one large array. A pointer is a thin abstraction over that address. Because a pointer can hold an address with no memory behind it, dereferencing it can crash the program. On x86 this is called a segmentation fault; on AMD64, dereferencing a non-canonical address raises a general protection fault. Some systems use segmentation or paging to map between physical memory and a smaller address space. Memory-mapped I/O lets some addresses refer to device registers rather than RAM.

## What pointers are used for

Pointers make repetitive operations cheaper: copying and dereferencing a pointer is faster than copying the whole datum. They are essential for traversing strings, lookup tables, linked lists, and trees; for holding addresses of subroutine entry points and dynamically linked library routines; and, in object-oriented languages, for binding methods through virtual method tables.

Three patterns recur across languages:

- **Pass-by-address.** Passing a pointer lets a function modify the caller's variable or return several values through its parameters.
- **Dynamic allocation.** Programs whose memory needs are not known at compile time allocate from the heap with routines like C's `malloc`, which returns a pointer; `free` returns the block. Forgetting to free blocks leaks memory.
- **Data-structure wiring.** Linked structures hold pointers to the next element, so the list can grow without moving existing data.

## Pointers in C

C exposes pointers directly because it was designed to map onto machine addresses.

```c
int a = 5;
int *ptr = &a;
*ptr = 8;
```

The `&` operator yields a pointer to its operand; unary `*` dereferences a pointer. In `int *ptr`, the `*` binds only to `ptr`, so `int *x, y;` makes `x` a pointer but leaves `y` as an `int`. C does not initialize pointer variables by default, so reading one before assignment is undefined behavior. Pointers are typically initialized to `NULL` or, since C23, `nullptr`; dereferencing a null pointer is also undefined.

C arrays and pointers are linked: the language requires that `a[i]` be equivalent to `*(a + i)`, because an array name decays to a pointer to its first element in most contexts. Pointer arithmetic moves by whole elements, so adding 1 to an `int *` on a machine with 4-byte ints advances the address by 4.

## Pitfalls and mitigations

Raw pointers can point anywhere, including uninitialized memory (a wild pointer) or freed memory (a dangling pointer). Dereferencing either is undefined behavior. Two pointers that compare equal are not always interchangeable: in C, C++, and LLVM the distinction is called provenance, and the optimizer may assume equal pointers came from the same chain of operations.

Languages mitigate these hazards in several ways:

- **Typed pointers and casts.** Assigning between pointer types of different kinds usually requires an explicit cast, catching mistakes at compile time. Arithmetic on typed pointers scales by the pointed-to type's size.
- **Opaque references.** Java and similar languages hide addresses behind references that can only access objects, never be used as numbers. Dereferencing a null reference throws an exception, and unreachable objects are reclaimed by garbage collection.
- **Smart pointers and ownership.** C++'s `unique_ptr`, `shared_ptr`, and `weak_ptr`, and Rust's `Box`, `Rc`, and `Arc` track ownership at runtime or compile time, freeing memory when the last reference dies. Rust's borrow checker enforces aliasing and lifetime rules, eliminating dangling pointers in safe code.
- **Iterators.** C++ iterators overload `++`, `*`, and `==` to behave like pointer operations without exposing addresses.
- **Multiple indirection.** A pointer to a pointer (e.g., `char **argv`) requires two dereferences to reach the data and is used when a function must modify the caller's pointer, such as inserting at the head of a linked list.

## Special kinds

- **Null pointer.** A reserved value indicating no object; marks end-of-list or allocation failure.
- **Dangling pointer.** Points at freed memory.
- **Wild branch.** A function pointer whose value is uninitialized or corrupted; calling it transfers control to an unpredictable address.
- **Function pointer.** Points to executable code, enabling callbacks and jump tables.
- **Autorelative pointer.** Stores an offset from its own address, so a structure containing one can be relocated without rewriting the offset.
- **Based pointer.** Stores an offset from another pointer, the base.
- **Pointer-to-member (C++).** Points to a field or method of a class, accessed with `.*` or `->*`.

## Support across languages

PL/I and C expose untyped or freely castable pointers with full arithmetic. Pascal restricts pointers to heap-allocated objects and forbids arithmetic. Ada uses typed access types with null defaults. Go allows pointers but no arithmetic and adds garbage collection. C# keeps C-style pointers behind `unsafe` while using `Span<T>` and `IntPtr` for managed access. Rust confines raw pointers to `unsafe` blocks and uses checked references otherwise. Java replaces pointers entirely with object references. Fortran-90 packages array bounds and stride inside the pointer object, so subscripting through it stays within those bounds.

A pointer is a small, indirect handle that a program can copy, pass, rearrange, and follow, and that low-level languages rely on to build the larger structures they manipulate.

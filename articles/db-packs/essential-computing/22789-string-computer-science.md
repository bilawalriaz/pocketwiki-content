# String (computer science)

A string is a finite, ordered sequence of symbols drawn from a fixed set called an *alphabet*. In programming, the alphabet is usually the characters a computer can represent, and a string holds text, identifiers, or any human-readable data a program reads, displays, stores, or accepts from a user. The term also extends to sequences of bytes or bits, so "string" can refer to any sequence of homogeneously typed data, not just text.

## Two design choices

Every string implementation is shaped by two decisions.

**Length: fixed or variable.** A fixed-length string reserves the same memory regardless of content, with the maximum chosen at compile time. A variable-length string grows and shrinks as needed, bounded in practice by available memory. Most modern languages use variable-length strings.

**Mutability: mutable or immutable.** In C++, Perl, and Ruby, the contents of a string can change in place, so the string is *mutable*. In Java, JavaScript, Python, Lua, and Go, any change produces a new string, so the string is *immutable*. Immutability costs extra copying but makes strings safe to share between threads. Languages with immutable strings often add a mutable companion, such as Java's `StringBuilder`, for code that builds text by repeated concatenation.

## How strings are stored

In memory, a string is an array of bytes, characters, or *code units*, the fixed-size pieces a particular encoding uses. The practical question is how the string records its length.

**Null-terminated.** The string ends with a reserved byte, traditionally the null character `0x00`, and length is not stored. C uses this convention: an *n*-character string occupies *n* + 1 bytes. The terminator byte cannot appear inside the data, so the string cannot carry arbitrary binary content, and forgetting the terminator invites buffer overruns.

**Length-prefixed.** The string begins with a number giving its length. Pascal's original strings used a one-byte prefix, capping length at 255; modern implementations use a 16-, 32-, or 64-bit word, lifting the cap to the address space. Length-prefixed strings can store any byte, including embedded nulls, and make length queries O(1). When the length field itself grows, the encoding is *succinct*: storing *n* symbols takes *n* + log(*n*) space.

**Dope vector.** Length and other metadata live in a separate descriptor. IBM's PL/I(F) compiler used this layout before later adopting length prefixes.

A few languages, notably Haskell, implement strings as linked lists of characters, trading fast random access for cheap structural sharing.

## Character encoding

A string is only as useful as its encoding. Early programs assumed one byte per character using ASCII or EBCDIC, which worked for Latin letters, digits, and a few punctuation marks. Logographic scripts such as Chinese, Japanese, and Korean (CJK) need thousands of glyphs, so older systems used two-byte codes for CJK characters alongside single-byte ASCII. Encodings like Shift-JIS and ISO-2022 were not self-synchronizing, meaning a byte in the middle of a string could not be identified as a leading or trailing byte without scanning back to the start, and slicing in the middle of a multi-byte character produced garbage.

Unicode, and especially its dominant byte format UTF-8, fixed these problems. UTF-8 is self-synchronizing: no byte from 0x00 to 0x7F ever appears as the trailing byte of a multi-byte sequence, so finding a character boundary is always possible by scanning forward. A Unicode code point occupies one to four bytes in UTF-8, and a visible character (a grapheme) can consist of several code points, so a string's *logical* length in characters can differ from its *physical* length in bytes. UTF-32 makes every code point exactly four bytes, which simplifies indexing but wastes space for ASCII-heavy text. Most modern APIs expose Unicode strings, though APIs that treat code units as if they were characters remain a common source of bugs.

## Formal definition

In formal language theory an alphabet Σ is a finite set of distinct symbols. A *string over Σ* is any finite sequence of those symbols. Its *length* |*s*| is the number of symbols, and may be any non-negative integer. The unique string of length 0 is the *empty string*, written ε or λ. Σ^* (the Kleene closure of Σ) denotes the set of all strings of every length, including ε. A *formal language* is any subset of Σ^*, for example the set of binary strings containing an even number of zeros.

The central operation is *concatenation*: given strings *s* and *t*, *st* is the symbols of *s* followed by the symbols of *t*. Concatenation is associative but not commutative, with ε as its identity. Σ^* and concatenation form a *free monoid*, and the length function is a monoid homomorphism because |*st*| = |*s*| + |*t*|.

A *substring* of *t* is a string *s* such that *t* = *usv*; a *prefix* has *u* empty and a *suffix* has *v* empty. A *palindrome* equals its own reverse, including ε and every single-character string. A *rotation* of *s* = *uv* is the string *vu*. If Σ has a total order, strings inherit *lexicographic order*, the dictionary order, though this order is total but not well-founded: the set {1, 01, 001, 0001, …} has no smallest element. The *shortlex* order, which compares by length first, fixes that and is well-founded.

## Security

Two vulnerabilities trace directly to how strings are stored. A missing terminator in a C-style string lets adjacent memory be read or overwritten, the classic *buffer overflow*. A manipulated length field in a length-prefixed string lets code read or write past the intended boundary, so safe access requires bounds checking. Strings from outside the program, such as form input, must be validated before interpretation, because unvalidated input is the standard vector for *injection* attacks, in which text meant as data is executed as instructions or queries.

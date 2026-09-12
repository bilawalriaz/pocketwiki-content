# Digital data

Digital data is information represented as a string of discrete symbols, each drawn from a finite alphabet such as letters or digits. The most common form in modern systems is binary data: a string of bits, each of which can be 0 or 1. A text document is a sequence of alphanumeric characters; a digital clock's display shows discrete digits rather than the continuously varying true time.

The contrast is with analog data, which is represented by a value from a continuous range of real numbers and can vary continuously with time. Sound pressure in air is analog. Turning an analog signal into digital requires *sampling* (measuring the value at regular intervals) and *quantization* (rounding each measurement to the nearest allowed symbol). The gap between the true value and the stored symbol is the *quantization error*, and the number of symbols chosen for a value sets the precision, a property called *granularity*.

Symbols are easier to digitize than analog signals because they are already discrete. A keyboard arranges its switches in a scan matrix and polls the x and y lines in sequence; when it detects a connection, it reports a scan code to the CPU, which translates it into a character using an encoding such as ASCII. Custom encodings avoid data loss for symbols (like 'ß') that standard encodings may not include.

## Three states of data

Every piece of digital data exists in one of three states, and confidentiality, integrity, and availability must be managed across all of them.

*Data at rest* is stored on media such as hard drives, SSDs, tapes, USB sticks, or cloud storage. It is protected chiefly by encryption (AES or RSA), access controls, and tokenization, which replaces sensitive values with meaningless stand-ins that preserve type and length so legacy systems can still process them.

*Data in transit* is moving across a network, either public (the internet) or private (a LAN). Without protection, copies of copies accumulate no noise and can be reproduced indefinitely, so encryption in transit is standard. Errors in digital transmission are substitution, insertion, or deletion of symbols, and a single uncorrected error can corrupt the entire message.

*Data in use* is actively being processed, held in volatile memory (RAM), CPU caches, or registers. Because it contains live secrets such as encryption keys, compromising it can unlock everything else. Defenses include memory encryption (AMD's Secure Memory Encryption from 2017, Intel's Total Memory Encryption and SGX enclaves), kernel patches that keep keys in CPU registers, and cryptographic tools such as homomorphic encryption, which compute on encrypted data without exposing it.

## Representation, keys, and structure

A bit is the smallest unit in memory, grouped into bytes or words at numbered addresses. A single datum is a value stored at a specific location, but the value is meaningless on its own: every datum needs a key that gives it context. In RAM the key is a hardware address; in a file it is a path and offset; in a database it is a value in one column that identifies a whole row.

Larger collections are organized into structures: arrays, tables, graphs, objects, or hierarchical trees such as the folders of a file system or an XML document. When the same structure repeats, a *control break* marks where a key value changes during sequential processing, which makes aggregation easy. Indexes (typically B-trees or hash tables) copy out keys and their locations into an inverted-tree structure so a small subset can be retrieved without scanning the whole dataset. Databases add a further layer of abstraction, using metadata and a query language so client and server can exchange data transactionally. Modern large-scale systems, such as Apache Hadoop, distribute data across many machines, and the machine's identity becomes part of the key so identical values on different nodes stay distinguishable.

## Programs are data too

A computer follows a sequence of instructions given to it in the form of data; that sequence is a program. In normal execution a program is machine code, but compilers, linkers, debuggers, virus scanners, and interpreters all treat other programs as their input data. Executable files can also contain a data segment of constants and initial values, and the line between code and data is exploited by both metaprogramming and malware.

## Properties of digital communication

All digital communication shares four practical properties. It needs *synchronization* (spaces and punctuation in text, special bit patterns in machine protocols) so the receiver can find the start of a message. It requires a *formal language* that both sides already share, defining the alphabet, allowed symbol sequences, and their meanings. It tolerates noise up to a point: small disturbances leave the symbols intact, but a large enough disturbance causes a symbol to be misread or the sequence to slip, and the resulting error can have an outsized effect on meaning. Digital data is *compressible*: uncompressed bits are bulky, but compression shrinks them for transmission and they are expanded again at the destination, which is why digital television carries more channels than analog within the same spectrum.

## History and scale

Digital encoding predates electronics. DNA stores genetic information in discrete base pairs; smoke signals, beacon fires, flag semaphore, maritime signal flags, and Morse code all use a small set of distinct states. The abacus, created between 1000 BC and 500 BC, represents numbers with beads in discrete positions. The word "digital" was used by Bell Labs mathematician George Stibitz in 1942 to describe the fast electrical pulses of an anti-aircraft gun controller, and it derives from *digitus*, the Latin word for finger, the original counting tool.

The scale has shifted rapidly. In 1986 less than 1% of the world's stored technological information was digital; by 2002 more was stored in digital than analog form, and by 2007 the figure was 94%, with roughly 281 exabytes of digital data in existence that year.

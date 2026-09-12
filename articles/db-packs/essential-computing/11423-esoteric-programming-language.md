# Esoteric programming language

An esoteric programming language (esolang) is a language designed to test the boundaries of language design rather than to write practical software. Designers build them as proof of concept, as software art, as a hacking interface into a host language, or as a joke. The label "esoteric" marks them as separate from the languages working developers use. Usability is rarely a goal; designers often strip conventional features while keeping the language Turing-complete (capable in principle of computing any computable function), or even intentionally leave its computational class unknown. Esolangs attract hackers, hobbyists, and computer science academics, and a few features, such as live code visualisation, have fed back into practical art tools.

## Origins

The canonical example is INTERCAL, created in 1972 by Don Woods and James M. Lyon as a parody of the languages they knew: FORTRAN, BASIC, COBOL, ALGOL, SNOBOL, SPITBOL, FOCAL, SOLVE, TEACH, APL, LISP, and PL/I. It existed only as photocopied manuals until a 1990 C implementation under Unix sparked wider interest in deliberately odd languages.

In 1993, Wouter van Oortmerssen wrote FALSE, a small stack-oriented language with a 1024-byte compiler built to make code inherently unreadable. Urban Müller's Brainfuck, an even tinier eight-character descendant, and Chris Pressey's Befunge, which adds a two-dimensional instruction pointer, together became the most-supported esolangs and the textbook examples of minimal Turing tarpits (languages small enough to fit in a programmer's head but awkward for real work). Brainfuck is related to the P′′ family of Turing machines.

## Common traits

Three patterns recur. Parody of mainstream conventions: INTERCAL spoofs 1960s languages, Shakespeare spoofs Elizabethan drama, Ook! spoofs Brainfuck by replacing its commands with orangutan sounds. Extreme minimalism: Brainfuck uses only eight single-character commands, Boolfuck operates on single bits, and Whitespace uses only spaces, tabs, and linefeeds, the characters most languages ignore, allowing programs to hide inside normal-looking source. Deliberate difficulty: Malbolge was explicitly built to be hard, with self-modifying code and operations whose effect depends on memory address.

Data representation often diverges from conventional variables. Brainfuck and Malbolge expose a single movable pointer. Befunge and Shakespeare use one or more stacks, executing in a Reverse Polish style (operators follow their operands, so `3 4 +` means "push 3, push 4, add"). Other languages explore number systems: TriINTERCAL replaces bits with base-3 ternary digits.

Instruction representation also varies. Befunge and Piet arrange programs in two dimensions, so control flow can move in any direction. Others disguise instructions as familiar text: Shakespeare reads as plays, Chef reads as recipes, Velato encodes instructions in MIDI files as intervals between notes. Some Chef programs function simultaneously as a recipe and as a working program, a property called multicoding; aesthetically balanced multicoding has been compared to the constraint-based writing of the Oulipo movement.

## Selected languages

- **Befunge**: instructions sit on a 2D grid with a pointer that can travel in any direction; Befunge-93, named for its 1993 release, is the most common version.
- **Brainfuck**: eight characters (`+ - < > . , [ ]`) operate a tape of cells with a moving pointer; all other characters are comments.
- **Chef**: a stack-oriented language by David Morgan-Mar where programs read as cooking recipes with ingredient lists.
- **FRACTRAN**: a program is an ordered list of positive fractions plus a starting integer *n*; at each step, *n* is multiplied by the first fraction that yields an integer, then the process repeats, and it halts when no fraction produces an integer. Invented by John Conway.
- **INTERCAL**: "Compiler Language With No Pronounceable Acronym," built in 1972 to satirise the conventions of 1960s languages.
- **JSFuck**: valid JavaScript written using only the six characters `[ ] ( ) ! +`, runnable in any browser; it has been used in cross-site scripting attacks, including against eBay, to slip past filters.
- **LOLCODE**: syntax modelled on lolcat speech, with conventional semantics.
- **Malbolge**: named after the eighth circle of Hell, designed to be maximally difficult through self-modifying code and address-dependent operations.
- **Piet**: programs are bitmaps of coloured regions; a pointer walks from region to region, and the hue and brightness steps between regions encode each instruction. Named after Piet Mondrian; the original name was already taken by a statistics package.
- **Shakespeare**: programs read as Shakespearean plays.
- **Unlambda**: a minimalist functional language built on SKI calculus (a tiny system of combinators equivalent to full computation) with first-class continuations (saved execution states that can be resumed later) and imperative I/O.
- **Velato**: MIDI files are the source code; the interval between successive notes relative to a chosen root determines each instruction.

## Cultural reading

Scholars such as Geoff Cox frame esolangs as cultural expression, akin to code art and code poetry, that shifts attention "from command and control toward cultural expression and refusal." Daniel Temkin argues that esolangs are "open-ended systems, natively collaborative, and distanced from any single materialized form," a counterpoint to the neutral professional style that Edsger Dijkstra advocated in *The Humble Programmer*.

Source: adapted from "Esoteric programming language" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Esoteric_programming_language

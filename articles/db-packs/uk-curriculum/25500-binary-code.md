# Binary code

Binary code is a data-encoding convention represented in binary notation: a sequence of 0s and 1s called a **bit string**. It covers both readable encodings like ASCII and non-human-readable forms like machine code and bytecode. Although all modern computer data is binary, other bases are commonly used to represent it: hex and octal are popular because they are powers of 2, making conversion to and from binary direct. ASCII characters, for instance, are often shown as decimal or hex rather than as raw bits; image data is typically hex, rarely decimal.

## Core idea

A binary encoding assigns meaning to patterns of two distinguishable states. The **bit** is the single unit; 8 bits make a byte. ASCII is a 7-bit encoding that maps numbers 0–127 to letters, digits, punctuation, and control operations. The letter "a" is decimal 97, rendered as the bit string `1100001`.

In **binary-coded decimal (BCD)**, each decimal digit gets its own 4-bit nibble. Since 4 bits can represent 16 values but only 10 (0–9) are valid, any nibble above 9 is illegal in BCD.

## How binary became the foundation

Gottfried Leibniz formalised the modern binary number system in 1689 in his paper *Explication de l'Arithmétique Binaire*, using only 0 and 1. He saw binary numbers as symbolic of *creatio ex nihilo* (creation out of nothing) and believed all logical and arithmetic reasoning could be reduced to binary form. Though he found no immediate practical use, his system is the direct ancestor of modern binary code.

Earlier binary-like systems existed independently. The Indian scholar Pingala (5th–2nd century BC) developed a binary system for prosody (poetic meter) in the *Chandashutram*. The Chinese *I Ching* hexagrams map onto binary numbers 0–63 through the duality of yin and yang; Leibniz, learning of them through Jesuit Joachim Bouvet, saw this as confirmation of his ideas. Francis Bacon (1605) proposed reducing alphabet letters to binary sequences that could be hidden as font variations, noting the scheme works with any objects capable of "a twofold difference only."

The bridge from abstract math to computing came through **Boolean algebra**. George Boole (1847) published an algebraic system of logic (AND, OR, NOT) built on a binary, yes-no foundation. It remained theoretical until Claude Shannon, an MIT graduate student, recognised that Boolean algebra behaves like electric circuits. His 1937 master's thesis, *A Symbolic Analysis of Relay and Switching Circuits*, made that connection explicit and launched the practical use of binary code in computers, circuits, and communication. By 1936, Alan Turing had already described machines that scan and process binary code in his paper "On Computable Numbers."

## Binary in the physical world

Any two distinguishable states can carry binary information. **Braille** uses a six-dot grid, each dot either raised or flat, to encode letters, numbers, and punctuation by touch.

Binary code endures not because two states are the only option, but because they are the most noise-resistant and easiest to build reliably in hardware. That practical simplicity, first formalised by Leibniz and activated by Shannon, is why modern computing is built on bits.

Source: adapted from "Binary code" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Binary_code

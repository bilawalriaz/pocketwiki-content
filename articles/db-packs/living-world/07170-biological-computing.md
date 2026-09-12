# Biological computing

A biological computer (biocomputer) is a system built from biologically derived molecules, primarily DNA and proteins, that performs digital or real-number computations. Nanobiotechnology, the engineering of biological parts at the 1–100 nanometer scale, provides the tools to assemble them.

## How a biocomputer works

Every biocomputer follows the same logic. A designer engineers a molecular pathway that, given certain input conditions (chemicals, light, or electrical signals), reacts to produce a measurable output read as the result.

The output signal varies by class, which gives the main taxonomy. Biochemical computers read the presence or concentration of specific molecules as the output, with feedback loops from catalytic enzymes, reactant levels, or binding molecules letting designers wire chemical networks that behave like logic circuits. Biomechanical computers read the three-dimensional shape a molecule adopts under the input conditions, with different conditions folding the molecule differently. Bioelectronic computers read the electrical conductivity of designed biomolecules, which conduct electricity in highly specific ways depending on the input.

## Boolean logic in chemistry

Tom Knight of the MIT Artificial Intelligence Laboratory proposed treating a chemical concentration as a binary signal: above a threshold equals 1, below it equals 0. Engineering a reaction pathway so the correct binary output appears only under specific initial conditions performs a logical operation. W. L. Ditto extended this in 1999 at Georgia Tech with a biocomputer made of leech neurons that performed simple addition.

Chemically induced dimerization, in which a chemical signal triggers two proteins to bind and produce an observable change in a cell, lets researchers build cell-based logic gates from individual cells.

## Network-based biocomputation

A distinct approach uses self-propelled biological agents, such as actin filaments pushed by myosin or microtubules pushed by kinesin, to explore a nanofabricated network encoding a mathematical problem. Channels etched into wafers by electron-beam or nano-imprint lithography guide the filaments; surface silanization anchors the motor proteins. When adenosine triphosphate (ATP) is added, the filaments move, converting chemical energy into mechanical motion.

The paths taken or the exits visited correspond to candidate solutions. Nicolau et al. demonstrated this on SUBSET SUM, an NP-complete problem, where every visited exit is a correct answer. A 2016 experiment showed the method scales to instances with 8 candidate solutions. Because ATP-to-motion conversion is highly efficient, each step uses orders of magnitude less energy than an electronic operation, and many filaments explore the network in parallel.

## Building with proteins and DNA

A protein's chemistry is dictated by its amino-acid sequence, which is itself dictated by the DNA nucleotides coding for it. Ribosomes read RNA and assemble the corresponding protein. The engineering implication is direct: design a DNA sequence, and the cell manufactures the protein components for the biocomputer. Synthetic DNA strands can also act as computational elements directly. The 2013 Stanford team led by Drew Endy used this principle to build the "transcriptor," a biological transistor that completed the three requirements for a functional biocomputer: data storage, information transmission, and a basic system of logic.

In July 2017, collaborators from Arizona State's Biodesign Institute and Harvard's Wyss Institute built a "ribocomputer" inside *E. coli* that responded to a dozen inputs, and separately archived images and movies in living *E. coli* DNA. In 2021, Sangram Bagh's team used *E. coli* to solve 2×2 maze problems, demonstrating distributed computation among cells.

## Why biology is economically interesting

Biological systems self-replicate and self-assemble. A single DNA molecule inside a cell can be copied many times, and each copy can direct the synthesis of every protein needed for a reaction pathway. A biocomputer built from these proteins could be produced in bulk from cell cultures without dedicated assembly lines, lowering cost compared to the manual fabrication of silicon chips.

## Recent commercial systems

In 2024, FinalSpark, a Swiss startup, launched a platform letting researchers run experiments remotely on biological neurons in vitro. In March 2025, Cortical Labs released CL1, the first commercially available biological computer: hundreds of thousands of lab-grown human neurons sustained for up to six months by an internal life-support system, interfaced with silicon hardware. The neurons run code through a Biological Intelligence Operating System (biOS), learn in real time inside a closed loop, and target drug discovery, disease modeling, and neuromorphic research while drawing far less power than conventional AI hardware. The Biological Computing Company, headquartered in San Francisco, emerged from stealth in February 2026 using living neurons to improve AI inference efficiency.

## Limits and outlook

Existing biocomputers perform simple Boolean and arithmetic operations and remain far less capable than commercial electronic machines. The motivation for scaling them up is twofold: massively parallel operation with a tiny energy budget per step, and a self-replicating supply chain. Whether biological substrates can be made dense, reliable, and programmable enough to challenge silicon remains the open question.

Source: adapted from "Biological computing" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Biological_computing

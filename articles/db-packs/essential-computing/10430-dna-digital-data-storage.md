# DNA digital data storage

DNA stores binary data by mapping bits onto strings of the four nucleotide bases, adenine, thymine, cytosine, and guanine (A, T, C, G). Writing a file means translating the bits into a nucleotide sequence, synthesising that sequence as physical DNA, and storing it; reading means sequencing the molecule to recover the nucleotide order, then translating back to bits. A gram of DNA can in principle hold hundreds of petabytes, and dry, cool DNA can remain readable for centuries, so archives that would fill a data centre could fit in a speck. In practice, synthesis and sequencing are still far too slow and expensive for routine use, which is why DNA is currently a niche medium for very long-term, rarely accessed archives rather than a replacement for disk or tape.

## How bits become nucleotides

Two design choices dominate every encoding scheme: how to convert bits to bases, and how to make the result robust against synthesis and sequencing errors.

For simple text, each letter can be mapped to a short codon (a triplet of nucleotides) drawn from a lookup table, the same trick the biological genetic code uses.

For arbitrary binary files, the bits are first converted to base-3 digits called trits, because three values fit neatly into the four available bases. Each trit is then mapped to a base, but the mapping is context-dependent: the table for the next nucleotide depends on the base just written, which prevents long homopolymers (runs of the same base such as AAAAA) that sequencers misread. A representative table:

| Previous base | trit 0 | trit 1 | trit 2 |
|---|---|---|---|
| T | A | C | G |
| G | G | T | A |
| C | C | G | T |
| A | A | C | G |

So if the previous base is T and the next trit is 2, the base written is G.

Two further techniques are standard. First, the data is split into many short overlapping strands, each labelled with an index sequence so the pieces can be reassembled in order; overlapping the strands by design means every region of the original data is covered several times, so a few damaged molecules can be reconstructed from their neighbours. Second, redundancy is added explicitly with error-correcting codes such as Reed–Solomon, and extra "synchronisation" bases are sprinkled in to act as landmarks during reconstruction.

A 2013 EBI study stored over five million bits with 99.99–100% accuracy using such overlapping oligonucleotides (short synthetic DNA strands) with built-in addressing. The 2017 DNA Fountain method of Erlich and Zielinski reached 215 petabytes per gram at roughly 85% of the theoretical Shannon capacity. Costs that year were about $7,000 to write two megabytes and $2,000 to read them back, so encoding theory has essentially solved density while the chemistry has not.

## Storing data inside living cells

Instead of synthesising free-floating DNA, data can be written into the genome of a living cell. Engineered bacteria carry molecular recorders, sometimes light-controlled recombinases, that flip small segments of DNA in response to a stimulus, marking which cells saw which signal. Each cell-culture well then acts as a biological bit. CRISPR gene editing can also splice artificial sequences directly into a genome, and proof-of-concept systems have recorded light-based images and text into engineered E. coli this way.

## Milestones

The idea is older than the technology. In 1959 Richard Feynman speculated about building machines at molecular scale, and in 1964–65 the Soviet physicist Mikhail Neiman published three papers independently proposing information storage on synthesised DNA and RNA. The first artwork stored in DNA was a 1988 collaboration between artist Joe Davis and Harvard researchers, who encoded a 5×7 pixel Germanic rune for "life and the female Earth" into E. coli.

The 2011 Church experiment stored a 659 kilobase book by mapping two bases to each binary digit, leaving 22 errors. The 2012 follow-up stored a 53,400-word HTML book, eleven JPEGs, and a JavaScript program at about 5.5 petabits per cubic millimetre, but used a naïve one-base-per-bit code that produced error-prone homopolymer runs. The 2013 EBI result showed that overlapping strands plus error correction could push accuracy near 100%. In 2015 ETH Zurich showed DNA encapsulated in silica-glass spheres could survive intact for long periods, and in 2016 Church and Technicolor stored 22 megabytes of MPEG-compressed video with zero retrieval errors. By 2018 Microsoft and the University of Washington had demonstrated random access over about 200 megabytes, and by 2019 a fully automated end-to-end encode/decode pipeline existed. In June 2019 all 16 GB of English Wikipedia were encoded into synthetic DNA, and in 2021 CATALOG reported a custom writer reaching 1 Mbps (128 KB/s). The same period saw the first album stored in DNA, Massive Attack's Mezzanine, and a DNA-of-things proof of concept that embedded a 3D-printed Stanford bunny's own blueprint into its plastic filament, readable by clipping off a fragment of its ear.

A 2021 Newcastle University study implemented a last-in, first-out stack data structure in DNA using strand displacement, showing that operations such as push and pop are possible in the molecular realm.

The bottleneck for routine use is no longer the encoding theory but the chemistry of synthesis and sequencing, which still costs orders of magnitude too much and runs too slowly to replace disk or tape outside of long-term archives.

Source: adapted from "DNA digital data storage" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/DNA_digital_data_storage

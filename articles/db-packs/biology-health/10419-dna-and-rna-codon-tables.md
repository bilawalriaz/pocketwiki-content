# DNA and RNA codon tables

A codon is three nucleotide letters read in a fixed order. The standard genetic code has 64 codons; almost all specify one of 20 amino acids, and the rest signal the ribosome to start or stop translation. The full mapping from triplet to amino acid or signal is the **codon table**. Because the same table underlies most genes in most organisms, it is the central reference for moving from a DNA or mRNA sequence to a protein.

## How to read the table

The table is a 4 × 4 × 4 grid. The first letter fixes the row, the second the column, and the third the sub-square. Rows and columns follow the order U, C, A, G in RNA (or T, C, A, G in DNA), and the reading direction is always 5′ to 3′ on the **sense strand**, the DNA strand whose sequence matches the mRNA read by the ribosome.

**Codon to amino acid.** Find the three letters in the grid; the cell gives the amino acid. UUU and UUC both encode phenylalanine, UCU through UCG and AGU/AGC encode serine, and UGG encodes tryptophan.

**Amino acid to codons.** Most amino acids have more than one codon, often differing only in the third position. The inverse table groups synonymous codons with IUPAC ambiguity letters: GCN (GCU, GCC, GCA, GCG) is alanine, and UUY (UUU, UUC) is phenylalanine. Methionine (AUG) and tryptophan (UGG) are the only amino acids with a single codon each.

**DNA versus RNA.** The two tables are identical except for one letter: DNA uses thymine (T), RNA uses uracil (U). Substitute T for U when converting an mRNA codon to its DNA form, or U for T in the reverse direction.

## Start and stop signals

UAA, UAG, and UGA do not encode an amino acid. They are **stop codons**, historically named *ochre*, *amber*, and *opal*, and they trigger the ribosome to release the finished polypeptide. They have no inverse entry; a stop simply terminates translation.

AUG is the standard **start codon**: it encodes methionine and, when recognised by an initiation factor, also begins translation. In rare contexts, GUG or UUG can act as starts. These normally encode valine and leucine, but a ribosome initiating at GUG or UUG still recruits methionine (or formyl-methionine in bacteria). The inverse table lists these alternative starts as HUG.

## Redundancy and the second position

Synonymous codons tend to share their first two letters and vary in the third, so amino acid groupings cluster when the table is read column-wise. Reorganising the grid by the second letter (and reordering to UCAG) instead of the first puts codons for chemically similar amino acids next to each other, arranged by side-chain hydrophobicity. The second position is the strongest predictor of whether the encoded amino acid is hydrophobic, polar, basic, or acidic, while the first and third positions tolerate more change. This pattern suggests early ribosomes prioritised the second position to control the hydrophobic core of folding proteins.

## The code is not truly universal

The code evolves. In 1981, mammalian mitochondria were shown to reassign several codons: AUA codes for methionine instead of isoleucine, and UGA codes for tryptophan instead of stop. Ciliates reassign UAA and UAG to glutamine. In yeast mitochondria, all four CUN codons encode threonine instead of leucine. Vertebrate mitochondria use AGA and AGG as stops rather than arginine, and echinoderm mitochondria use AAA for asparagine instead of lysine. Recent screens of bacterial genomes have uncovered further variants, including CGG reassigned to glutamine, tryptophan, or arginine in different bacterial lineages.

Alternative assignments are catalogued in numbered **translation tables**: the standard nuclear code is table 1, vertebrate mitochondrial is table 2, yeast mitochondrial is table 3, and ciliate nuclear is table 6, with additional tables covering mould, invertebrate, echinoderm, ascidian, and other mitochondrial and nuclear codes. Differences from the standard code are concentrated in a small set of codons, especially AUA, UGA, AGA, AGG, and the CUN family, because reassignments spread only after a codon becomes rare or disappears from a genome. The same 64-triplet grid is therefore reused, but a few cells carry different amino acids or signals depending on the genome being read.

Source: adapted from "DNA and RNA codon tables" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/DNA_and_RNA_codon_tables

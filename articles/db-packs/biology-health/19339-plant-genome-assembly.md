# Plant genome assembly

A plant genome assembly is the complete genomic DNA sequence of a plant species, reconstructed into chromosomes and organelle genomes from short DNA fragments produced by sequencing machines. Assembling one is harder than assembling a human genome because plant genomes are unusually large, repetitive, and frequently polyploid.

## Why plant genomes are hard to assemble

Plant genome size and structure vary dramatically. Green algae start near 15 million base pairs (Mbp), while loblolly pine reaches roughly 22 billion base pairs (Gbp), one of the most complex assemblies available. Two features drive the difficulty:

- **Repetitive DNA from mobile genetic elements (MGEs).** MGEs are DNA sequences that can move around the genome. They divide into class I retrotransposons, which copy themselves through an RNA intermediate, and class II DNA transposons, which cut and paste directly. In plants, long-terminal-repeat (LTR) retrotransposons predominate and can make up 15% to 90% of the genome. Repetitive tracts often exceed 10 kilobase pairs (kbp), longer than a typical sequencing read, so short reads cannot place them uniquely.

- **Polyploidy**, meaning more than two complete sets of chromosomes in one cell. About 80% of plant species are polyploids, so many chromosomes look nearly identical and are hard to distinguish during assembly.

These features explain why early next-generation sequencing (NGS) assemblies fragmented into many contigs (continuous consensus sequences built from overlapping reads) with unfinished regions.

## Milestones and scale

The first plant genome completed was *Arabidopsis thaliana* in 2000, the third multicellular eukaryote sequenced after *C. elegans* and *Drosophila melanogaster*. Arabidopsis was chosen because its nuclear genome is small (135 Mbp, about 4% the size of the human genome) and its generation time is short (8 weeks). The Arabidopsis Genome Initiative delivered 115.4 Mb of finished sequence and 25,498 protein-coding genes.

Rice (*Oryza sativa*) followed through the International Rice Genome Sequencing Project, which began in September 1997 and targeted the smallest major cereal genome at 400–430 Mb. Between 2000 and 2008, ten plant genomes were published; in 2012 alone, thirteen appeared. NCBI now lists more than 400 plant genomes, of which 72 have been re-annotated.

## Assembly strategies

Different technologies defined different eras of plant genomics.

**Sanger clone-by-clone (BAC-by-BAC).** A physical map of each chromosome is built first. The genome is broken into large fragments, each inserted into a bacterial artificial chromosome (BAC), a DNA vector carried inside bacteria for stable propagation, and amplified. The BAC inserts are sheared into smaller overlapping pieces, sequenced, and assembled into contigs placed onto the chromosome map using the original landmarks. Related vectors include P1-derived artificial chromosomes (PACs), yeast artificial chromosomes (YACs), and transformation-competent artificial chromosomes (TACs). For Arabidopsis, end sequences from 47,788 BAC clones extended contigs from anchored BACs, and 1,569 clones formed a minimum tiling path. Maize (*Zea mays*, 2.3 Gb, 10 chromosomes) used 16,848 minimally overlapping BACs combined with cDNA and methylation-filtered libraries, DNA preparations enriched for low-methylation, gene-rich regions. Clone-by-clone reduces computational load and handles repetitive DNA well, but costs ran between $70 million and $200 million per assembly.

**Sanger whole-genome shotgun (WGS).** DNA is randomly sheared, cloned, and sequenced from both ends without any prior map. Computational tools assemble overlapping reads into contigs and supercontigs, larger scaffolds built by linking contigs with paired-end data. Grapevine (*Vitis vinifera*) used this approach, producing 20,784 contigs into 3,830 supercontigs with an N50 of 64 kb (the contig length above which half the total assembly length lies) and a total size of 498 Mb. Later improvements enabled papaya, *Brachypodium distachyon*, sorghum, soybean, and cottonwood (*Populus trichocarpa*).

**Next-generation sequencing (NGS).** Cheap short reads from platforms such as Illumina are usually combined with Sanger data or long reads. Cucumber (*Cucumis sativus*) used 72.2-fold coverage (3.9-fold Sanger, 68.3-fold Illumina GA), producing 243.5 Mb anchored to seven chromosomes. Cacao (*Theobroma cacao*, 2010) blended 454 and Illumina reads with Sanger BAC reads, yielding 25,912 contigs and 4,792 scaffolds (ordered groups of contigs linked by paired-end evidence) covering 326.9 Mb, about 76% of the estimated genome. Similar hybrid strategies produced the first apple (*Malus domestica*), cotton, sweet orange, and domesticated tomato genomes.

**Third-generation sequencing (TGS).** Single-molecule platforms such as PacBio RS II produce reads up to 54 kbp, long enough to span most plant repeats, though raw error rates around 10% require redundant coverage and short-read polishing. Spinach was an early plant example, achieving a 63-fold improvement in contig size over an Illumina-only assembly. A recent improved apple assembly combined PacBio long reads, Illumina paired-end and mate-pair reads (two reads from a single insert of known size, useful for spanning repeats), SOAPdenovo and DBG2OLC assemblies, BioNano optical mapping (long-range physical maps from imaging stretched DNA in nanochannels), and 15,417 SNP markers to anchor 649.7 Mb of scaffolds, producing a 643.2 Mb final assembly closer to the estimated genome size than earlier drafts.

## Databases

Several resources distribute these assemblies. Ensembl Plants holds reduced representations of about 45 sequenced plant species with gene models and polymorphism data. Gramene adds comparative genomics and pathway analysis on Ensembl infrastructure. PGDBj integrates ortholog (genes in different species descended from a common ancestor), DNA marker, linkage, and germplasm data for model and crop plants. PlantsDB supports comparative queries across multiple species. PLAZA focuses on evolutionary analyses across the green plant lineage (Viridiplantae). TAIR remains the dedicated resource for the Arabidopsis reference genome.

The shift from BAC-by-clone to shotgun to NGS to long-read hybrid assemblies tracks both falling cost and the need to span the repetitive, polyploid structure that defines plant genomes.

Source: adapted from "Plant genome assembly" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Plant_genome_assembly

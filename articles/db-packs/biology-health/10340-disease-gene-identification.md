# Disease gene identification

Disease gene identification is the process of pinpointing which mutant genotypes cause an inherited genetic disorder. Mutations can be single nucleotide substitutions, small insertions or deletions, complete deletion of a gene, or other structural abnormalities.

Knowing which gene causes a disorder simplifies patient diagnosis and reveals how the mutation disrupts normal function. Modern high-throughput sequencing, combined with the data resources of genomics, has made identification faster and able to resolve more complex mutations than older methods allowed.

## General workflow

Most strategies follow the same skeleton. First, DNA is collected from several patients believed to share the same genetic disease. Second, the samples are screened to highlight probable regions where the mutation could lie. Third, these regions are aligned across samples, and the overlapping segment is taken as the most likely location of the disease gene. If enough reference sequence is available, candidate genes in that region are examined and their coding portions are sequenced until a mutation is found. Adding more patients or families narrows the region further.

The differences between most techniques lie in the second step: how researchers screen DNA to flag probable regions.

## Pre-genomics approaches

Before whole-genome sequences were common, researchers worked with little prior knowledge of the regions they examined. They used genetic markers such as Restriction Fragment Length Polymorphism (RFLP) analysis and microsatellite analysis to compare samples.

Loss of heterozygosity (LOH) analysis compares two samples from the same individual, typically a tumor sample and a matched normal control. RFLPs and microsatellite markers reveal whether a region is heterozygous (carrying two different alleles) or homozygous (carrying two identical copies). When the disease arises from deletion of one copy of a gene, the control sample appears heterozygous at that locus while the tumor sample appears homozygous. That shift marks the disease gene's location.

## Post-genomics approaches

High-throughput sequencing and genome-wide analysis software have made sequence acquisition cheaper and faster, expanding the gene-hunting toolkit.

### Identity by descent (IBD) mapping

IBD mapping uses single nucleotide polymorphism (SNP) arrays to scan polymorphic sites across the genomes of affected individuals and their relatives. A region is identical by descent when a run of contiguous SNPs shares the same genotype. Comparing an affected individual to an affected sibling highlights shared identical regions. Comparing the same affected individual to an unaffected sibling removes any region identical in both, since the unaffected sibling does not share the disease. Repeating this across multiple families yields a small overlapping fragment that should contain the disease gene.

### Homozygosity and autozygosity mapping

Homozygosity mapping is valid only when the mutation segregates within a small, closed population, often one shaped by a founder effect, where a small ancestral group gives rise to a larger population with limited genetic diversity. Such populations have a limited gene pool, so an inherited disease is likely caused by two copies of the same ancestral mutation on the same haplotype (a set of variants inherited together on one chromosome). Affected individuals are therefore homozygous across the relevant region. SNP arrays survey the genome, homozygous blocks from affected individuals are overlaid, and the overlap is taken as the disease gene's location.

Autozygosity mapping extends this by considering population allele frequencies. Plotting a cumulative LOD score, a statistical measure of how strongly the data support linkage to a location, alongside the homozygous blocks confirms the result and can distinguish between suspicious regions: a homozygous block caused by an inherently non-diverse stretch of the genome yields a very low LOD score and can be set aside. Tools such as HomSI identify homozygous stretches directly from next-generation sequencing data.

### Genome-wide knockdown studies

Genome-wide knockdown studies are a reverse-genetics strategy, one that starts from the genome and works backward to phenotype, enabled by whole-genome sequences and gene-silencing technologies such as siRNA (small interfering RNA, short molecules that degrade specific messenger RNAs) and deletion mapping. Researchers systematically knock down or delete genes, usually in prokaryotes or tissue culture because the scale is enormous. After confirming knockdowns, often by checking mRNA expression, they observe the resulting phenotypes. Samples whose phenotypes match the disease point to the knocked-down genes as candidate disease genes.

### Whole exome sequencing

Whole exome sequencing uses modern sequencing and DNA assembly to reconstruct all coding portions of the genome, then compares them to a reference genome. After filtering out known benign polymorphisms, synonymous changes (mutations that alter a codon but not the amino acid it specifies), and intronic changes (non-coding stretches within a gene) that do not affect splice sites, only potentially pathogenic variants remain. Exome sequencing can be combined with other techniques, such as IBD or homozygosity mapping, to exclude additional candidates.

## Choosing a method

The right technique depends on the disease's inheritance pattern and the population structure of the affected families. LOH suits paired tumor and normal tissue from one individual. IBD mapping fits families with multiple affected and unaffected siblings. Homozygosity and autozygosity mapping are reserved for diseases in small, closed populations where founder effects are likely. Genome-wide knockdown and whole exome sequencing are general-purpose tools that do not require prior family structure. In every case, the workflow stays the same: collect DNA, screen for probable regions, align them across samples, and sequence the overlap until the causal mutation emerges.

Source: adapted from "Disease gene identification" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Disease_gene_identification

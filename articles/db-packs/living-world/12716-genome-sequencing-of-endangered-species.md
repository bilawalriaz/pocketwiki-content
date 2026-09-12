# Genome sequencing of endangered species

Conservation biology has long relied on captive breeding and private farming. These work in some cases, but breeding from few individuals shrinks the genetic pool and raises inbreeding. Genome sequencing adds another tool: read the DNA of threatened animals and plants, then guide management from what the genome reveals.

A genome is the complete set of an organism's DNA. Sequencing means reading the order of its chemical letters (A, T, C, G). Next Generation Sequencing (NGS) runs millions of parallel reads, dropping the cost enough to apply to wildlife rather than only to humans or model organisms.

## Why read a threatened genome

Conservation genetics asks questions that fieldwork cannot answer directly:

- How many distinct populations exist and how do they relate? Whole-genome comparison of the Dryas monkey placed it as a sister lineage to the vervet monkey, with bidirectional gene flow between roughly 750,000 and 500,000 years ago.
- Is the population still diverse, or already inbred? The same Dryas monkey study, based on fewer than 250 remaining adults, found high diversity and low inbreeding with low genetic load.
- When did this species split from a close relative? A chromosome-level assembly of the golden snub-nosed monkey placed its divergence from the Rhesus macaque at about 13.4 million years ago and improved the genome roughly 100-fold, producing 22,497 protein-coding genes.
- What is the sex of an individual when appearance cannot tell? Sex identification is hard in amphibians, where many species carry homomorphic sex chromosomes (X and Y look alike) and genomes are large.
- Which DNA variants matter for survival? Genome-wide association studies (GWAS) link specific variants to fitness, local adaptation, inbreeding depression, or disease susceptibility, and help evaluate how a population might respond to a changing environment.

## Practical methods

Whole-genome sequencing is data-intensive. For many conservation questions, researchers instead sample a small, representative slice. Restriction site-associated DNA sequencing (RADseq) cuts the genome at specific short sequences and reads only those fragments. Double digest RADseq (ddRADseq) uses two enzymes so the slice is more reproducible. These reduced-representation approaches let labs score thousands of SNP markers (single positions where individuals differ) across many animals at modest cost.

For plants flagged as PSESP (Plant Species with Extremely Small Population), DNA comes from fresh leaves and RNA from stems, roots, fruits, and buds. The RNA reveals the transcriptome, the set of genes currently expressed, which helps assemble and annotate the genome. Software then scaffolds contigs (assembled sequence fragments) into chromosomes and identifies orthologous genes, genes inherited from a common ancestor, for cross-species comparison.

## The Japanese giant salamander

The Japanese giant salamander (Andrias japonicus) and other Cryptobranchidae have genomes around 56 Gb. Their sex chromosomes are homomorphic and have switched between XY (male-determining) and ZW (female-determining) systems many times, a lability called heterogamety, where one sex carries two different sex chromosomes.

Using ddRADseq on known-sex individuals (sex previously established by ultrasound, laparoscopy, and serum calcium differences), researchers identified new sex-linked loci. They tested both male and female heterogamety by checking which loci appeared only in one sex, then confirmed candidates with PCR (targeted DNA amplification) on additional known-sex samples. The result supported female heterogamety across several divergent Cryptobranchidae populations, resolving the ambiguity for captive breeding.

## Limits and open problems

Two bottlenecks remain. Sampling: collecting DNA can stress fragile animals or damage rare plants. Workarounds include radio-collar monitoring to gather opportunistic samples and growing primary cell cultures from biopsies, lab-grown cells that can be resampled without re-handling wild animals. Analysis: sequencing has become cheaper and faster than the bioinformatics and population-genetics methods that interpret it, and turning genomic findings into on-the-ground conservation strategy remains difficult.

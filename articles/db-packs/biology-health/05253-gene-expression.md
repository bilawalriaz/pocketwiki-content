# Gene expression

A gene is a stretch of DNA. Gene expression is the process that turns that DNA information into a working molecule the cell can use, almost always a protein, sometimes a functional RNA. Each cell carries the same genome, yet a liver cell, a neuron, and a skin cell look and behave differently because they express different sets of genes at different times. Controlling which genes are on, how strongly, and when is what allows a single genome to build a whole organism and to respond to a changing environment.

## The central pathway in three steps

For a protein-coding gene the flow of information is DNA → RNA → protein.

1. **Transcription.** RNA polymerase reads the template DNA strand (3′→5′) and builds a complementary RNA strand (5′→3′), adding one ribonucleotide at a time. Uracil (U) replaces thymine (T). Transcription starts at a DNA region called the promoter and stops at a terminator.
2. **mRNA processing (eukaryotes only).** The initial transcript (pre-mRNA) is modified before use. A 7-methylguanosine cap is added to the 5′ end, a poly(A) tail of roughly 200 adenines is added to the 3′ end after cleavage at an AAUAAA signal, and non-coding introns are removed by the spliceosome while exons are joined. These changes protect the RNA, help it leave the nucleus, and allow alternative splicing, in which one gene produces several different mRNAs and therefore several different proteins.
3. **Translation.** The ribosome reads the mRNA in triplets called codons. Each codon matches an anticodon on a transfer RNA (tRNA) carrying a specific amino acid, and the ribosome joins the amino acids into a chain that folds into a protein. A typical mammalian mRNA is translated into around 2,800 protein molecules.

In prokaryotes there is no nucleus, so transcription and translation occur on the same mRNA at the same time and the mRNA needs little processing. A prokaryotic mRNA often carries several proteins' worth of information (polycistronic); eukaryotic mRNAs usually carry one (monocistronic).

## Non-coding RNA genes

Many genes do not code for protein. The transcribed RNA is itself the functional product. Ribosomal RNAs and tRNAs are required for translation; small nuclear and small nucleolar RNAs (snRNAs, snoRNAs) help with splicing and rRNA modification; microRNAs (miRNAs) regulate other genes. These RNAs are usually made as longer precursors and trimmed. For example, pri-miRNA is cut in the nucleus by Drosha into a ~70-nucleotide stem-loop pre-miRNA, exported, then cut in the cytoplasm by Dicer into a short mature miRNA loaded into the RISC complex with Argonaute protein.

## Regulation

Any step of the pathway can be tuned.

| Level | How it is controlled | Effect |
|---|---|---|
| Chromatin / DNA | Histone modifications; DNA methylation at CpG sites; euchromatin is open and transcribed, heterochromatin is compact and silent | Makes a gene accessible or inaccessible to RNA polymerase |
| Transcription | Transcription factors bind enhancers, silencers, and insulators. Enhancers sit far away and loop to the promoter, stabilized by dimeric connectors such as CTCF; the Mediator complex passes the signal to RNA Pol II | Turns transcription rate up or down; about 1,600 transcription factors operate in a human cell |
| RNA processing and export | Alternative splicing, 5′ cap, poly(A) tail, nuclear export controls | Changes which protein is made and how stable the mRNA is |
| mRNA stability and translation | miRNAs binding the 3′UTR, RNA interference, poly(A) tail length | Each human miRNA typically targets several hundred mRNAs; over 60% of human protein-coding genes have conserved miRNA pairing sites |
| Protein | Post-translational modifications: phosphorylation, acetylation, glycosylation, ubiquitination; proteolytic cleavage | Activates, deactivates, relocates, or marks a protein for destruction |

Some genes, called **constitutive** or **housekeeping** genes (for actin, GAPDH, ubiquitin), are on continuously in all cells to keep basic machinery running. **Facultative** or **inducible** genes are switched on only when needed, for example insulin in response to rising blood glucose, or cyclins to drive the cell cycle.

## Measuring expression

Gene expression is measured either by counting mRNA or by counting protein.

- **mRNA methods.** Northern blotting separates RNA by size on a gel and detects a target with a labelled probe. RT-qPCR reverse-transcribes mRNA into cDNA and amplifies it, giving sensitive absolute counts down to single molecules. RNA-Seq uses next-generation sequencing to read every transcript in a sample, and can discover new genes and splice variants.
- **Protein methods.** Western blotting uses antibodies to detect a specific protein on a membrane, giving size as well as identity. ELISA uses antibodies in microplate wells for more accurate quantification. Fusing a protein to green fluorescent protein (GFP) allows live-cell imaging of where and when it appears.

mRNA levels are not a perfect proxy for protein levels, because translation and protein stability also shape the final amount. The most informative studies measure both. Because the same gene can be spliced in several ways, decorated by different modifications, and regulated at many levels, a human genome of roughly 20,000 protein-coding genes can produce a proteome many times larger and a much greater range of cell types than the gene count alone would suggest.

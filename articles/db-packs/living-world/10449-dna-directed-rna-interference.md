# DNA-directed RNA interference

DNA-directed RNA interference (ddRNAi) is a gene-silencing technique that uses a DNA construct delivered into a cell to switch on the cell's own RNA interference (RNAi) machinery. The cell then keeps transcribing the construct and replenishing its silencing RNA, so knockdown lasts far longer than injecting pre-made silencing RNA. Any RNA can be targeted, including host messenger RNAs (mRNAs) and RNAs from infecting viruses, by encoding a sequence complementary to the target.

## How the construct works inside a cell

A typical construct is a small DNA piece with four parts in order: a promoter (an "on switch" host enzymes recognise), a sense sequence, a short loop, an antisense sequence, and a terminator ("stop signal"). The sense and antisense sequences are each 20–30 nucleotides and are exact complements, so the RNA transcribed from the construct folds back on itself into a short-hairpin RNA (shRNA), one strand with a double-stranded stem and a loop. Host enzymes (Drosha and Dicer) cut the shRNA into small interfering RNAs (siRNAs). One strand of each siRNA loads into the RNA-induced silencing complex (RISC), which then binds any RNA matching the sequence and destroys it.

Because the DNA sits in the nucleus and is transcribed continuously, the cell keeps making new siRNA, the key practical difference from synthetic siRNAs, which are used up within days. ddRNAi can sustain knockdown for months in dividing cells and longer in non-dividing cells.

## Construct variants

A multi-cassette construct expresses two or more different shRNAs from the same DNA, either as separate transcription units or as a single long hairpin with several stems. Targeting multiple sites on one viral RNA matters because RNA viruses such as HIV mutate rapidly; a single point mutation can otherwise let a viral genome escape silencing. Multi-cassette designs can also combine shRNAs with other therapeutic RNAs, such as ribozymes (RNAs that cut other RNAs catalytically) and decoy RNAs that soak up viral proteins.

## Delivery

Getting the construct into the right cells is the central practical obstacle. Two broad strategies exist: viral vectors, including lentiviruses (retroviruses that infect non-dividing cells) and adeno-associated virus (AAV, a small virus that mostly stays outside the host genome), which enter cells efficiently but raise safety concerns; and non-viral transfection reagents, such as modified polyethylenimine, a positively charged polymer that condenses DNA into particles cells take up. Constructs can be delivered in vivo (directly into the patient) or ex vivo (cells are taken out, treated in culture, then returned). Ex vivo delivery limits whole-body vector exposure and was the route used in most early clinical work.

## Applications

HIV/AIDS. In a phase I trial at the City of Hope National Medical Center, four HIV-positive patients with non-Hodgkin's lymphoma received their own hematopoietic progenitor cells (blood-forming stem cells) transduced ex vivo with a lentiviral vector carrying a triple construct. It expressed an shRNA against the HIV tat and rev genes (regulatory genes the virus needs to replicate), a CCR5 ribozyme that blocks viral entry, and a TAR decoy that blocks viral transcription. shRNA expression was still detectable in T cells, monocytes, and B cells more than a year after transplantation.

Hepatitis B. Biomics Biotechnologies screened roughly 5000 siRNA sequences against the HBV polymerase gene (the virus's own replication enzyme) and selected five that worked as shRNAs. They are combined into a multi-cassette construct, Hepbarna, delivered by an AAV-8 vector that homes to liver.

Neuropathic pain. The investigational construct Nervana targets protein kinase C gamma (PKCγ), a signalling enzyme whose overexpression is linked to neuropathic pain and morphine tolerance. Two conserved PKCγ sequences (identical across rats, mice, and humans) were identified, and cassettes were built against each. In cultured cells, PKCγ expression fell 80%. In a rat neuropathic-pain model, intrathecal injection (into the spinal fluid) of a lentiviral vector carrying the construct produced pain relief.

Drug-resistant non-small-cell lung cancer. Resistance to paclitaxel and cisplatin in non-small-cell lung cancer (NSCLC) is associated with overexpression of beta III tubulin, a microtubule protein variant. shRNA knockdown of beta III tubulin slowed tumour growth and restored drug sensitivity in mouse models. The triple-cassette construct Tributarna delivers three shRNAs against this target via a modified polyethylenimine vector (jetPEI) designed to accumulate in lung tissue.

Oculopharyngeal muscular dystrophy (OPMD). OPMD is a rare late-onset muscle disease with no approved treatment, caused by a mutation in the PABPN1 gene. The disease is driven by a gain-of-function mutation, so silencing the mutant gene with ddRNAi is a plausible strategy.

## Safety concerns

Insertional oncogene activation. Some vectors, particularly early retroviruses, integrate into the host genome at random and can land next to an oncogene (a gene that, switched on inappropriately, drives cancer), activating it. This caused lymphoid tumours in early gene-therapy trials. AAV vectors are considered low risk because they mostly stay outside the genome and have shown no cancer link in decades of natural human infection. Lentiviral vectors do integrate but do not preferentially activate oncogenes.

Immune response to the vector. An early trial patient died from a severe immune reaction to an adenoviral vector, so preclinical screening for vector-directed antibodies and careful dose escalation are now standard.

Innate immune activation by siRNAs. Some siRNAs trigger toll-like receptors (TLRs), cell-surface sensors of microbial patterns that normally set off interferon (an antiviral signalling protein) defences. Because ddRNAi constructs are delivered into the cell interior, they bypass these surface sensors and are not expected to trigger this response.

Toxicity from shRNA overexpression. Pushing shRNA production too high saturates the endogenous RNAi machinery, which can disrupt the cell's own microRNA pathways and cause liver damage or death. Strategies to control this include using weaker or inducible promoters and engineering shRNAs that Dicer processes more precisely.

Off-target silencing. Any shRNA with partial complementarity to other transcripts can knock down unintended genes, with unpredictable effects. Careful sequence selection and preclinical screening reduce but do not eliminate this risk.

Source: adapted from "DNA-directed RNA interference" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/DNA-directed_RNA_interference

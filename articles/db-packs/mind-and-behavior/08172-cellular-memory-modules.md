# Cellular memory modules

Cellular memory modules are DNA sequences that let a cell remember which genes should stay on or off long after the original signal is gone. They are a form of **epigenetic inheritance**, heritable information carried on top of the DNA sequence itself. After cell division or development, daughter cells inherit not just genes but their activity state, so a liver cell keeps behaving like a liver cell and a neuron keeps behaving like a neuron. That preserved state is implemented through **transcriptional memory**, the cell's capacity to remember past gene-expression decisions. Cellular memory modules are best characterised in the fruit fly *Drosophila*, where the underlying protein machinery was first worked out.

## Discovery

In 1961 at the Pasteur Institute in Paris, François Jacob and Jacques Monod discovered cellular memory modules while mapping how genes self-regulate, turning on when their product is needed and off when it is not. They also showed that genetic information travels from DNA to the protein-building machinery through a messenger molecule, later identified as RNA. The work earned Jacob, Monod, and André Lwoff the 1965 Nobel Prize in Physiology or Medicine for discoveries concerning genetic control of enzyme and virus synthesis. Lwoff contributed to the Nobel-winning work on virus synthesis but did not take part in the cellular memory experiments, which is why his name is not attached to the original discovery.

## How they work

The core idea is that genes undergo transcription in one environment, are transferred to a new cellular environment, and then revert to their original on or off state because that state is physically preserved on the chromosome.

Two opposing protein families carry this out:

- **Polycomb group (PcG)** proteins bind to **Polycomb response elements (PREs)**, short DNA sequences in the fly genome. PcG excludes transcriptional activators and compacts the surrounding chromatin, blocking RNA synthesis and silencing the target gene.
- **Trithorax group (trxG)** proteins bind to corresponding trithorax response elements and do the opposite. They keep the chromatin open and the gene active.

The two systems are antagonistic, and which one wins at a given locus is what the cell remembers through division. The same general logic applies across species, but the specific proteins and DNA sequences that recruit PcG and trxG differ depending on where in the genome the module sits. PcG proteins are particularly important for keeping **Hox genes**, the master regulators of body-segment identity, switched off in segments where they should not be active.

Two well-studied *Drosophila* examples show how location-specific the mechanism can be.

**Ab-Fab (Abdominal-B / Fab-7 region).** Researchers identified a minimal 219-base-pair memory module from the Fab-7 region, which regulates the *Abdominal-B* Hox gene. The module recruits trxG proteins to binding sites on the **Zeste** protein, bypassing Zeste's usual need for the **Brahma (BRM)** chromatin remodeller and locking in an active chromatin state that is inherited through division. When the Zeste binding sites were mutated, Zeste's role in PcG-dependent silencing increased, and the Ab-Fab sequence was found to weaken PcG binding to Zeste, allowing chromatin to return to an active state. The DNA element was judged a true memory module because the same sequence carried memory of both the silent and the active state, and the two elements physically overlap on the chromosome.

**H3K27 (histone 3 lysine 27).** Early in *Drosophila* embryogenesis, the **Polycomb repressive complexes PRC1 and PRC2** are recruited to chromatin carrying the **H3K27me3** mark, a methyl group added to lysine 27 of histone H3. PRC2 catalyses this methylation, which in turn recruits more PRC1 and PRC2 and compacts the chromatin. PRC2 recruitment also depends on a nearby ubiquitin mark, **H2AKub**, on histone H2A. When the H3K27 residue was mutated, PcG proteins could still be recruited and the original silenced phenotype was restored, indicating that the cell can compensate through the recruitment machinery when the H3K27 mark is removed.

## Applications

**Synthetic memory devices.** Because cellular memory modules are built on the well-understood process of transcription, synthetic biologists have copied them to build artificial memory circuits. These synthetic devices can log whether a cell has experienced a particular stimulus, maintain a chosen gene-expression state over time, and tag cell populations so their response to an event can be tracked across divisions. The same approach is used to test suspected risk factors for disease. Exposing cells in a dish lets researchers observe physiological effects that would otherwise take years of human exposure to appear, which can guide public-health policy. A module can also feed its own output back as input, holding a desired protein level long term, which is useful in gene therapy.

**Cancer.** When PcG regulation fails, developmental programs can be reactivated in the wrong tissue. Because PcG proteins control cell-cycle progression, differentiation, and stem-cell plasticity, their misregulation can initiate **tumorigenesis**, and the link is especially strong in hormone-dependent cancers, where PcG proteins interact directly with hormone receptors. PcG proteins also reshape the metabolism and immune signalling of the tumour microenvironment, accelerating cancer progression, and the full chain of causation is still being mapped.

Source: adapted from "Cellular memory modules" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Cellular_memory_modules

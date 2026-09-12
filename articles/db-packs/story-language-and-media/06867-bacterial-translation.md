# Bacterial translation

Bacterial translation is the process by which a bacterial ribosome reads a messenger RNA and assembles the corresponding protein. A ribosome is the molecular machine that does the reading; mRNA (messenger RNA) is the copy of a gene that carries the protein-building instructions. Because bacteria lack a nucleus, the ribosome can attach to one end of an mRNA while RNA polymerase is still transcribing the other end, so transcription and translation run on the same mRNA at the same time.

The bacterial ribosome (70S) is built from a large 50S subunit and a small 30S subunit. It carries three functional sites: the A site, where each new aminoacyl-tRNA enters; the P site, which holds the tRNA carrying the growing polypeptide; and the E site, where the spent, uncharged tRNA exits. The first amino acid is N-formylmethionine (fMet), delivered by a special initiator tRNA. GTPases are GTP-binding enzymes that hydrolyze GTP to drive conformational work; several (IF2, EF-Tu, EF-G, RF3) power the bacterial translation cycle.

## Initiation: finding the start codon

In the canonical (Shine–Dalgarno) pathway, a short sequence called the Shine–Dalgarno (SD) sequence, located a few nucleotides upstream of the start codon, base-pairs with a complementary anti-SD stretch on the 16S rRNA of the 30S subunit. This recruits the small subunit and positions the start codon at the P site. Three initiation factors assist assembly: IF1 and IF3 bind the 30S and prevent premature 50S joining and tRNA entry into the A site, while IF2 (a GTPase) escorts the initiator fMet-tRNA into the P site. GTP hydrolysis then joins the 50S subunit to form the active 70S initiation complex.

The canonical rules have well-documented exceptions. The start codon is usually AUG, but E. coli uses GUG (in *lacI*) and UUG (in *lacA*), and studies have documented at least 17 non-AUG start codons in E. coli, with AUG still the strongest. Some mRNAs have no SD sequence at all; the entire phylum Bacteroidetes translates without one. An SD followed by AUG is also not always sufficient. Some mRNAs are "leaderless," with little or no 5′ untranslated region (UTR), and a complete 70S ribosome guided by IF2 can start directly at a 5′-phosphate-bearing start codon. A 5′ phosphate is near-essential for this route, and IF3 inhibits it.

On polycistronic mRNAs (single transcripts carrying several genes), a 70S ribosome that has just finished a coding sequence does not always split apart. It can scan forward along the mRNA until it finds the next SD sequence and downstream start codon, then reinitiate with IF2 and IF3. This 70S scanning mode is thought to matter most when neighboring genes sit close together on the same transcript.

## Elongation: building the chain one amino acid at a time

Elongation adds amino acids to the carboxyl end of the growing chain through a repeating three-step cycle.

1. A-site decoding. An aminoacyl-tRNA is delivered to the A site by EF-Tu (a GTPase). The ribosome uses large conformational changes (conformational proofreading) to test and reject incorrect pairings, which is the main reason protein synthesis is slow.
2. Peptide bond formation. The 50S subunit contains a ribozyme, the 23S rRNA, which catalyzes transfer of the growing peptide from the P-site tRNA onto the amino acid on the A-site tRNA. The resulting A-site species is a dipeptidyl-tRNA; the P-site tRNA is now deacylated.
3. Translocation. EF-G (a GTPase) shifts the ribosome by one codon, moving the deacylated tRNA to the E site (where it leaves during the next A-site loading) and the peptidyl-tRNA to the P site, exposing a fresh codon in the A site.

The protein exits through the polypeptide exit tunnel of the 50S subunit, and the cycle repeats codon by codon.

## Termination: ending the chain

When a stop codon (UAA, UAG, or UGA) enters the A site, no tRNA recognizes it. Release factors bind instead: RF1 recognizes UAA and UAG; RF2 recognizes UAA and UGA. They trigger hydrolysis of the ester bond linking the finished protein to the P-site tRNA. RF3 (a GTPase) then catalyzes release of RF1 or RF2 from the ribosome.

## Recycling: preparing the next round

The post-termination complex (mRNA, deacylated tRNA, and 70S ribosome) is disassembled by Ribosome Recycling Factor (RRF) together with EF-G, which split the ribosome into its 30S and 50S subunits. IF3 then displaces the deacylated tRNA from the 30S subunit, freeing all components for a new round.

## Polysomes and rate

Multiple ribosomes translate a single mRNA simultaneously; the resulting mRNA–ribosome assembly is a polysome (or polyribosome). Bacterial ribosomes polymerize proteins at about 18 amino acids per second, compared with roughly 1000 nucleotides per second for DNA replication. The gap reflects the larger 20-letter amino acid alphabet and the time spent rejecting wrong aminoacyl-tRNAs.

## Regulation during starvation

In stationary phase, E. coli downregulates translation. RMF (ribosome modulation factor) binds 70S ribosomes to form inactive 90S dimers, which HPF (hibernation promotion factor) matures into 100S particles whose two 30S subunits contact each other; RMF blocks mRNA binding by interfering with 16S rRNA. The related protein YfiA also binds the A and P sites, but its C-terminal tail blocks RMF, so YfiA-bound ribosomes stay as inactive 70S monomers. RsfS (formerly RsfA; the "S" denotes starvation) binds the large-subunit protein L14 and blocks 50S–30S joining. Under heat shock, the GTPase HflX instead splits stalled ribosomes by binding the peptidyl transferase center in a release-factor-like manner and prying the subunits apart.

## Antibiotics

Many antibiotics act on bacterial translation in ways that spare eukaryotic ribosomes, exploiting structural differences between the two kinds of ribosome.

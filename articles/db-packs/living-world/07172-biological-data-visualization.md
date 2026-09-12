# Biological data visualization

Biological data visualization is the branch of bioinformatics that applies computer graphics and information visualization to life-science data, including sequences, genomes, macromolecular structures, biochemical networks, microscopy images, and whole-body scans. A current trend is the merging of atomic-resolution 3D structures, cryo-electron microscopy of larger complexes, and whole-cell maps of protein location into unified views.

## Sequence alignment and phylogeny

Alignments arrange DNA, RNA, or protein sequences in columns so that identical or similar residues line up, with gaps inserted to optimize the match. A pairwise alignment compares two sequences; a multiple sequence alignment (MSA) extends this to many, identifying conserved regions, mutations, and evolutionary relationships. Aligned sequences are shown as a colored matrix, with a consensus row summarizing the most common residue at each position. A sequence logo encodes the same information graphically: total letter height at each position reflects conservation, and the relative size of each letter reflects its frequency, making DNA-binding motifs immediately visible. Circular or spiral MSAs handle genomes whose starting position is arbitrary, such as mitochondrial DNA and viroids. The 1D-3D Group Alignment Viewer at RCSB.org links MSAs to PDB structures, coloring experimentally determined residues blue and predicted regions by their confidence score (pLDDT).

Phylogenetic trees are branching diagrams of evolutionary relationships. In a cladogram, only topology matters. In a phylogram, branch length is proportional to the number of genetic changes, so deeper nodes are both older and represent more distant common ancestors. Circular layouts and 3D phylogeny explorers (which separate species relatedness from gene duplication events onto separate axes) pack more taxa into one view.

Common tools: Clustal Omega, MUSCLE, MAFFT, and T-Coffee compute alignments; Jalview, BioEdit, and Geneious edit and annotate them; FigTree, iTOL, and MEGA draw trees; UCSC Genome Browser and Ensembl display alignments against full annotated genomes.

## Macromolecular structure

Proteins, nucleic acids, carbohydrates, and their complexes are routinely visualized in 3D to relate structure to function. The RCSB Protein Data Bank (PDB), the US node of the Worldwide Protein Data Bank, archives experimentally determined structures and provides free web access.

Common methods include volume rendering, which reveals internal structure without segmentation; interactive 3D viewers with rotation and zoom; augmented and virtual reality for spatial immersion; and molecular dynamics animations that show conformational change. Hybrid techniques overlay experimental data (mutations, binding affinity) as heat maps on the structure.

Small and nanoscale objects need electron- and probe-based microscopy. Nanoparticles (1–100 nm), carbon nanotubes, nanofibers, and nanocomposites are typically imaged with transmission electron microscopy (TEM), scanning electron microscopy (SEM), or atomic force microscopy (AFM), with dynamic light scattering (DLS) giving size distributions and X-ray diffraction (XRD) confirming atomic arrangement.

Widely used molecular viewers include PyMOL, UCSF Chimera and ChimeraX, Jmol, VMD, Swiss-PdbViewer, Coot, BIOVIA Discovery Studio, and Schrödinger Maestro.

## Systems biology

Systems biology visualizes entire biochemical networks, metabolic pathways, gene regulation, and protein interactions rather than single molecules. Models are built as graphs of reactions whose rates are estimated from mass-action or enzyme kinetics and assembled into systems of differential equations. For metabolism, constraint-based methods such as flux balance analysis (FBA) find the steady-state flow of metabolites through a network given stoichiometric, enzymatic, and capacity constraints. Mass spectrometry imaging complements these models by mapping the spatial distribution of metabolites, peptides, and proteins across tissue, turning measured intensity into a 2D chemical image. Software includes massPy, Cytosim, PySB, Cytoscape for networks, and Medusa for genome-scale metabolic ensembles.

## Microscopy

Beyond optical and electron microscopy, biological samples are imaged with scanning probe, ultraviolet, infrared, digital holographic, and laser techniques. Two-photon microscopy images up to 800 μm into tissue by exciting fluorophores with paired long-wavelength photons, useful for tracking microrobots in vivo. Bright-field light microscopy with high-intensity pulsed LED illumination and 12-bit capture, corrected by spectroscopic calibration, can be displayed in 8-bit with minimal information loss. A community-driven initiative promotes the FAIR data principles (findable, accessible, interoperable, reusable) to raise microscopy standards in publications.

## Magnetic resonance imaging (MRI)

MRI forms pictures of internal anatomy by exploiting the magnetic properties of hydrogen protons. The sample sits in a strong magnetic field, aligning proton spins along the field axis. A radiofrequency (RF) pulse tips the magnetization away from alignment; as protons relax, they emit RF signals. Two relaxation times are measured: T₁, the return of net magnetization along the field, and T₂, the decay of transverse magnetization. Different tissues have characteristic T₁ and T₂ values, so pulse sequences that emphasize one or the other produce contrast:

- T₁-weighted: fluid black, muscle grey, fat white. Often combined with fat suppression to highlight anatomy.
- T₂-weighted: fluid white, muscle grey, fat white. Combined with fluid attenuation (FLAIR) to hide cerebrospinal fluid when looking for lesions.
- Proton density (PD): long repetition time, short echo time; useful for joint cartilage, now mostly replaced by FLAIR in brain imaging.

Variants extend what MRI can show. Magnetic resonance angiography images blood vessels, diffusion MRI traces water motion to map neuronal tracts (diffusion tensor imaging, DTI) or disentangle multiple fiber populations (diffusion basis spectrum imaging, DBSI), and functional MRI (fMRI) detects the blood-oxygen-level-dependent (BOLD) signal, the local ratio of oxygenated to deoxygenated hemoglobin, as a proxy for neural activity.

## Computed tomography and PET

CT uses X-rays; the denser the tissue, the more it attenuates and the brighter it appears. A radiocontrast agent enhances contrast: positive agents such as barium sulfate absorb X-rays and brighten vessels or the gut, while negative agents such as carbon dioxide appear dark. Acquisition modes include sequential (step-and-shoot), spiral (continuous rotation as the table moves), and electron beam tomography (electron paths steered by coils, with no mechanical rotation).

PET detects gamma rays from a positron-emitting radiotracer, so it images metabolism or receptor binding rather than anatomy. Different radiotracers target different processes. Radiotracers differ from radiocontrasts in that they are detected through radioactive decay rather than X-ray absorption. Modern scanners combine both as PET-CT, aligning functional and anatomical data in one session.

Maximum intensity projection (MIP) collapses a stack of 2D slices into a 3D-looking image by keeping the brightest voxel along each viewing ray, and is especially good at revealing small lung nodules, though respiratory and blood-flow artifacts can mimic disease. MIP also applies to MR angiography and, in research, to MRI, where neural networks have classified lesions from MIP MRI more accurately than from single slices.

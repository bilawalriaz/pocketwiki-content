# Biological network

A biological network represents a biological system as a set of entities (nodes) connected by interactions (edges). Edges may be undirected (a connection is present or absent) or directed (one node regulates another), and they can carry weights that encode interaction strength. Formally, a network is an N×N matrix whose entries are 0 or 1, or a real weight, where N is the number of nodes. Because the same graph formalism handles proteins, genes, species, neurons, or individuals, one framework can ask structural questions across biology.

## OriginsLeonhard Euler formalized graph theory in 1736 while solving the Seven Bridges of Königsberg problem. Random-graph theory followed in the mid-twentieth century, and by the mid-1990s it was clear that real biological and technological networks have structural properties random models do not reproduce. From the late 2000s onward, scale-free and small-world ideas reshaped systems biology, and graph-based methods are now applied directly to molecular interaction data.

## Major network types

**Protein–protein interaction (PPI) networks.** Nodes are proteins; edges are physical binding. Edges are undirected, so the two participants can be hard to identify. Yeast two-hybrid screens and mass spectrometry map interactions, and curated databases include BioGRID, IntAct, MINT, the Database of Interacting Proteins, the Human Protein Reference Database, and inference databases such as STRING and FunCoup. Proteins with many connections (hubs) are more likely to be essential for survival, showing that overall composition, not just pairwise interactions, matters.

**Gene regulatory networks (GRNs).** Nodes are genes and the transcription factors that control them. A directed edge from A to B means A regulates B and may represent activation or inhibition. The human genome encodes roughly 1,500 DNA-binding transcription factors regulating more than 20,000 genes. GRNs are built from curated databases such as Reactome and KEGG and from high-throughput methods including microarrays, RNA-Seq, ChIP-chip, and ChIP-seq.

**Gene co-expression networks.** Nodes are transcripts; edges represent statistical association of expression, often measured by Pearson correlation. Co-expression modules may correspond to cell types or pathways, and highly connected intramodular hubs serve as representatives of those modules.

**DNA–DNA chromatin networks.** Nodes are genomic loci; edges represent physical proximity or linkage. Edge weights can be derived from Genome Architecture Mapping (GAM) data. The mouse Hist1 region, a large cluster of replication-dependent histone genes whose organization is nearly identical to the human Hist1 cluster, is a worked example. Filtering and thresholding reduce noise, and highly connected hubs define communities of frequently interacting loci.

**Metabolic networks.** Nodes are small molecules such as carbohydrates, lipids, and amino acids; edges are enzyme-catalyzed reactions. Network analyses can be used to infer how selection shapes metabolic pathways.

**Signaling networks.** These integrate protein–protein interactions, gene regulation, and metabolism to transmit signals inside and between cells. The MAPK/ERK pathway, which travels from the cell surface to the nucleus via a chain of protein–protein interactions and phosphorylation events, is a canonical example. NicheNet models inter-cellular communication from single-cell data.

**Neuronal networks.** The brain's structural and functional connections are themselves small-world networks: most cortical areas can be reached from any other through only a few steps, as shown in primate cortex and in human swallowing.

**Food webs.** Nodes are species; edges are feeding interactions. Robustness tends to grow with connectance, the fraction of possible links that actually exist.

**Between-species ecological networks.** Pairwise interactions are extended to many species to study competitive and cooperative relationships. Plant–pollinator networks are mutually beneficial and exhibit nestedness (specialists interact with subsets of the species generalists use), redundancy, and modularity, properties that can buffer these networks against anthropogenic disturbance.

**Within-species social networks.** Edges represent associations between individuals and can encode aggressive, cooperative, or sexual interactions. In wire-tailed manakins, a male's degree (number of direct social partners) predicts his rise in the hierarchy. In bottlenose dolphins, betweenness centrality (the fraction of shortest paths between other dolphins that pass through a given individual) predicts who leads group travel using side flopping and upside-down lobtailing. Network analysis has revealed hidden dynamics such as the seasonal variability of female chacma baboon bonds.

## Network medicine

Network medicine applies these ideas to human disease. Rather than blaming single genes, it locates disease modules, interconnected groups of molecules whose collective dysfunction produces pathology, and uses the surrounding network to predict new disease genes, relationships between diseases, and multi-target therapies. The approach supports drug repurposing and the integration of large-scale omics data.

## How networks are analyzed

**Association.** Edges must be built from quantitative signals. Two widely used measures are Pearson correlation, which captures linear co-variation between two variables, and linkage disequilibrium, the non-random association of genetic variants at different loci on a chromosome.

**Centrality.** Centrality measures rank nodes by structural importance.

- *Degree centrality* counts a node's direct connections: C_D(i) = k_i. High-degree nodes are hubs.
- *Betweenness centrality* counts how often a node lies on shortest paths between other nodes: C_B(i) = Σ_{s≠t} σ_st(i) / σ_st. High-betweenness nodes bridge otherwise separate regions; in yeast, such proteins are more evolutionarily conserved and more often essential.
- *Closeness centrality* uses the average shortest-path distance from a node to all others: C_C(i) = (n − 1) / Σ_j d(i, j), so high-closeness nodes communicate efficiently.
- *Eigenvector centrality* awards a node credit for being connected to other well-connected nodes: A C_E = λ C_E, where A is the adjacency matrix and λ its largest eigenvalue.
- *Katz centrality* extends eigenvector centrality by summing contributions from all paths, with farther nodes contributing less: C_K(i) = Σ_j Σ_k α^k (A^k)_{ij} + β, where α controls how quickly distant influence decays and β gives every node a baseline score.

These measures answer different questions and are often reported together.

**Communities.** Many biological networks are modular. Community-detection algorithms partition nodes into groups with dense internal edges and sparse external ones. The Louvain method greedily maximizes modularity by repeatedly moving each node to the community that most increases that score. The Leiden algorithm refines this approach with faster merging and a refinement step, producing better-connected communities. A 2002 study of Chesapeake Bay marine mammals using this kind of method found a clear split between pelagic and benthic organisms.

**Network motifs.** Statistically significant recurring patterns of a few nodes, often 2 or 3, are network motifs. Motif analysis of directed functional brain networks built from resting-state fMRI has been used to study basic patterns of information flow in the human brain.

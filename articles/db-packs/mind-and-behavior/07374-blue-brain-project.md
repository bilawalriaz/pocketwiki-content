# Blue Brain Project

The Blue Brain Project was a Swiss research initiative that ran from May 2005 to December 2024 at the École Polytechnique Fédérale de Lausanne (EPFL). It aimed to build a biologically detailed digital reconstruction and simulation of the mouse brain in order to identify the principles that govern brain structure and function.

## Core approach

The project worked from the bottom up, beginning with the neocortical column. A neocortical column is a vertically organised bundle of neurons roughly 0.5 mm wide and 2 mm tall, often treated as a basic repeating unit of the neocortex. A human column contains about 60,000 neurons; a rat column is structurally similar but holds around 10,000 neurons and 10⁸ synapses (the junctions through which neurons signal each other). Modelling the rat column gave the team a testbed for the methods and data needed to reconstruct larger regions of the mouse brain.

Simulation ran on an IBM Blue Gene supercomputer using NEURON, a software environment originally written by Michael Hines for modelling the electrical behaviour of individual neurons. Each neuron was represented with biologically realistic ion channels and wiring, and the connections between neurons were derived from an empirical connectome, a map of which neurons connect to which. Over time the models incorporated additional cell types, including astrocytes, a class of support cells, and their metabolic coupling to neurons through the neuro-glia-vasculature (NGV) unit.

## Key milestones

- 2006: first model of a neocortical column, using simplified neurons.
- 2007: initial data-driven model of a rat neocortical column, marking the end of the project's first phase.
- 2015: simulation of a portion of a rat brain with about 30,000 neurons; first quantitative model of neuron–astrocyte energy coupling.
- 2017: the project used algebraic topology, a branch of mathematics that describes connectivity through shapes such as holes and cavities, to analyse neural networks. They found that groups of neurons, called "neural cliques," link into structures that occupy up to eleven dimensions.
- 2018: release of the first digital 3D cell atlas of the mouse brain, mapping cell types, numbers, and positions across 737 brain regions.
- 2019: the model of the whole mouse cortex was complete, with virtual EEG experiments planned. The model had grown so large that the team began exploring representing each neuron as a small artificial neural network.
- 2022: release of Topological Neuronal Synthesis, an algorithm that generates millions of unique cell morphologies from a few reference cells, enabling simulation of both healthy and diseased states and the long-term possibility of digital twins of brains.

Henry Markram founded and directed the project. He also conceived the Human Brain Project (HBP), funded in 2013 by the European Union with up to $1.3 billion, to which Blue Brain contributed. In 2009 Markram claimed a "detailed, functional artificial human brain" could be built within ten years, a prediction that did not materialise as stated.

## Open-source software tools

All Blue Brain software is open source and hosted on GitHub. Each tool addresses a specific bottleneck in reconstruction or simulation:

| Tool | Purpose |
|------|---------|
| Blue Brain Nexus | Knowledge-graph data platform following FAIR principles (Findable, Accessible, Interoperable, Reusable) for organising neuroscience data |
| BluePyOpt | Builds electrical models of single neurons by using evolutionary algorithms to fit parameters to experimental recordings |
| CoreNEURON | Optimised engine that boosts the speed and memory efficiency of NEURON for large-scale simulations |
| NeuroMorphoVis | Visualises neuron shapes reconstructed from microscopy |
| SONATA | A data format co-developed with the Allen Institute for exchanging large network models across platforms |

## Collaborations and funding

The Cajal Blue Brain Project, coordinated by Javier de Felipe at the Technical University of Madrid, ran parallel simulations on the Magerit supercomputer at the Supercomputing and Visualization Center of Madrid (CeSViMa). The project was funded mainly by the Swiss government and the European Commission's Future and Emerging Technologies (FET) Flagship grant, with additional private donations. EPFL acquired the Blue Gene prototype at a discount, and the project became a recognised test case for the Blue Gene architecture. The 2021 documentary *In Silico*, directed by Noah Hutton, tracked the project's shifting goals over the preceding decade.

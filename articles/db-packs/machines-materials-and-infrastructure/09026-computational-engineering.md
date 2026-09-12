# Computational engineering

Computational engineering develops and applies computational models for engineering problems. These models are called computational engineering models (CEM). The field uses computers to solve engineering design problems across many industries, drawing on computational geometry, virtual design, and simulation-driven workflows, and sometimes pairing numerical methods with elements of AI.

The core mechanism is an engineer encoding design knowledge into a computer program. That program becomes an algorithm, the CEM, which can generate many variants of an engineering design from varied inputs. Additional mathematical models then analyse the outputs, creating algorithmic feedback loops that steer the design toward better solutions. The same model can be re-executed against many requirements rather than a single fixed scenario.

Computer simulation gives the field a feedback channel that traditional experiments often cannot. A numerical model can probe conditions too expensive, too dangerous, or physically inaccessible to build, and it can do so cheaply enough to iterate. For this reason computational engineering overlaps heavily with computational science and engineering, a sibling field described as the "third mode of discovery," alongside theory and physical experimentation.

## How it differs from related fields

Computational engineering is not computer science, though it borrows algorithms, data structures, parallel programming, and high-performance computing from that field. It is also distinct from computer engineering, though some computer-engineering problems can be modelled and solved with CEM methods, treated as an application area rather than the core of the discipline.

## Methods and foundations

Computational engineering rests on a small set of technical pillars:

- High-performance computing, with efficiency gains from computer architecture choices and parallel algorithms.
- Modelling and simulation of physical and engineered systems.
- Algorithms for both discrete and continuous problems.
- Data analysis and visualisation.
- Mathematical foundations including numerical and applied linear algebra, initial and boundary value problems, Fourier analysis, and optimisation.
- Data science methods for extracting knowledge from large scientific datasets.

A few practical notes on tooling anchor these methods. FORTRAN remains the most widely used language in scientific computing because of its legacy codebase and simpler syntax, and the community has been slow to replace it. C++ and C have gained ground. The proprietary environment MATLAB is popular for rapid application development and model verification because of its natural expression of mathematical computations and built-in visualisation. Python, paired with NumPy, SciPy, and Matplotlib, has grown into a free alternative to MATLAB.

## Open-source tooling

A handful of free and open-source tools support the workflow. OpenSCAD, released in 2010, generates CAD models from scripts and can seed a computational engineering model. CadQuery uses Python to generate CAD models on top of the OpenCascade framework and is released under the Apache License. PicoGK is an open-source computational engineering framework, also under the Apache License.

## Applications across engineering

The same algorithmic feedback-loop pattern is applied to very different domains:

- Aerospace and mechanical engineering: combustion simulation, structural dynamics, computational fluid dynamics, computational thermodynamics, computational solid mechanics, vehicle crash simulation, biomechanics, and satellite trajectory calculation.
- Defence and security: battlefield simulations, military gaming, homeland security, and emergency response.
- Biology and medicine: protein folding and other macromolecule simulations, bioinformatics, genomics, computational neurological modelling, biological system modelling, 3D CT and MRI imaging, molecular bionetworks, and cancer and seizure control.
- Chemistry: structures and properties of molecules and solids, computational chemistry, cheminformatics, molecular mechanics, computational methods in solid-state physics, and chemical pollution transport.
- Civil engineering: finite element analysis, structures under random loads, construction engineering, water supply, and transportation modelling.
- Computer, electrical, and telecommunications engineering: VLSI, computational electromagnetics, semiconductor and microelectronics simulation, energy infrastructure, RF simulation, and networks.
- Environmental engineering and numerical weather prediction: climate research, computational geophysics including seismic processing, and natural disaster modelling.
- Industrial engineering: discrete event and Monte Carlo simulation for logistics and manufacturing, queueing networks, and mathematical optimisation.
- Nuclear engineering: reactor modelling, radiation shielding, and fusion simulation.
- Petroleum engineering: reservoir modelling, and oil and gas exploration.
- Physics: particle physics, automatic calculation of particle interaction or decay, plasma modelling, and cosmological simulation.

Each of these domains already relies on mathematical models, so wrapping them in a generative algorithm with feedback is often a small step, and the payoff is the same: designs that can be re-tuned by changing inputs rather than rebuilt by hand.

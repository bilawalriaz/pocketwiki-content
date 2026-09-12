# Computer-automated design

Computer-automated design (CAutoD) extends computer-aided design (CAD) beyond drawing and simulation: the computer itself searches for and refines good designs. The term first appeared in a 1963 paper in the IBM Journal of Research and Development, which described a program that searched for logic circuits satisfying hardware constraints and evaluated them by how well they discriminated characters in a recognition set. CAutoD applies broadly to automotive, civil, and structural engineering, composite materials, control systems, mechatronics, and the invention of new systems, and is increasingly driven by biologically inspired machine learning, including heuristic search techniques such as evolutionary computation and swarm intelligence algorithms.

## The design problem as a search

A design is a point in a high-dimensional space, one dimension for every adjustable parameter (a length, a material property, a controller gain). Each point has a quality score derived from the design's behaviour, and choosing the best design is equivalent to searching that space for the highest-scoring point.

This framing matters because physical prototyping is slow and expensive. CAutoD replaces repeated physical builds with "digital prototyping": a software model of each candidate is evaluated, scored, and improved many times before any hardware is made. The model can target several goals at once, such as maximising output, raising energy efficiency, raising speed, and cutting cost, so the search runs through a multidimensional, often multi-modal space (one with several distinct peaks), under either a single weighted objective or several competing ones.

## How the search is scored

For a single objective, quality is written as a cost function J (a value from 0 to infinity, lower is better) or as a fitness function f (a value from 0 to 1, higher is better), with the conversion f = J / (1 + J). If J is differentiable (its slope can be computed at every point) in a manageable space, the optimum can in principle be found analytically: locate every point where the first derivative of J is zero and the second derivative confirms a minimum or maximum, check the boundaries, and pick the best. In real engineering, however, the score is usually noisy, non-numerical, or multi-objective, so gradients are unreliable or do not exist, and analytical methods break down. Much refinement is still done by hand, with a designer adjusting parameters in a CAD simulation and judging the result, often many times, until the design is "good enough."

## How the search is automated

The adjustment loop can in principle be replaced by exhaustive search, checking every possible combination of parameters. Because the number of combinations grows exponentially with the number of parameters, exhaustive search quickly becomes impossible: a design with only 30 binary choices has over a billion candidates, and real designs have far more.

A practical alternative is a biologically inspired evolutionary algorithm (EA), a non-deterministic polynomial-time algorithm (running time grows as a polynomial of the input size) that mimics natural selection. Each candidate is encoded as a string of numbers, a chromosome. A population of candidates is scored by the same simulation a human would use, often run in batch mode alongside an existing CAD package. To form the next generation, the algorithm keeps the best performers (survival of the fittest, a form of a posteriori learning, where performance is judged after evaluation), then creates new candidates by crossover (swapping parameter values between two parents) and mutation (randomly perturbing some values). Over many generations the population improves on average.

An EA run can start from a database of existing designs or from a randomly generated population, and the top candidates after convergence are the optimised digital prototypes. Public tools such as EndlessForms, which evolves 3D objects that can be 3D-printed, and PicBreeder, which does the same for 2D images, show this interactive evolutionary process in action.

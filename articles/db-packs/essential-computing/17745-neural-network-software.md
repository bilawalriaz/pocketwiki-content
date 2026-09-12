# Neural network software

Neural network software simulates, trains, and applies artificial neural networks, computational systems loosely patterned on biological neurons. Most modern tools fall into four overlapping categories: simulators, development environments, custom code built on programming libraries, and standards for exchanging models.

## Simulators

A neural network simulator runs a neural network inside a self-contained application, usually with visualization of the training process and sometimes of the network's physical structure. Simulators focus on a limited set of network types and are not designed to export a trained model into other software.

Research simulators investigate network behavior and properties. Historically dominant, they have largely been replaced in artificial network research by general component-based development environments, but they remain the main tool for studying biological networks, where the simulation models neural tissue, chemistry, and electrical impulses between neurons. Common artificial network simulators include the Stuttgart Neural Network Simulator (SNNS) and Emergent. Common biological network simulators include Neuron, GENESIS, NEST, and Brian.

Data analysis simulators target practical applications such as data mining and forecasting. They typically use a fixed, configurable network — most often a backpropagation network or self-organizing map — and include preprocessing. They are easy to use but less flexible than general development environments. Neural Designer is a representative example.

Teaching simulators trace back to the 1986–87 Parallel Distributed Processing (PDP) volumes and their accompanying software, which required no programming. That software evolved into PDP++ and then into Emergent, gaining power at the cost of complexity. In 1997, tLearn returned to a small, beginner-friendly design supporting basic feed-forward and simple recurrent networks trained by backpropagation; it was last updated in 1999. In 2011, Basic Prop, a self-contained platform-neutral JAR file, offered similar simple functionality.

## Development environments

Development environments differ from simulators in two ways: they support custom network architectures and they can deploy a trained network for use outside the environment. They often include advanced preprocessing, analysis, and visualization.

Component-based environments are the dominant modern style. The network is built by wiring adaptive filter components in a pipe-and-filter flow, with the data flow controlled by an exchangeable control system. This lets developers assemble custom networks, mix adaptive with non-adaptive components, and ship the result. Built on frameworks such as .NET and Java, these tools can deploy networks as inheritable components, and some target embedded systems. Examples include Peltarion Synapse, NeuroDimension NeuroSolutions, Scientific Software Neuro Laboratory, and the LIONsolver integrated software. Free open-source options include Encog and Neuroph. The trade-off is greater complexity than a simulator and a steeper learning curve.

## Custom implementations and libraries

Many practitioners skip both simulators and environments and implement networks directly. Basic network types are straightforward to code, and programming libraries such as TensorFlow and Theano supply neural network functionality with bindings for languages like Python, C++, and Java.

## Standards: PMML

For a model trained in one application to be reused in another, a shared representation is needed. The Predictive Model Markup Language (PMML), an XML-based standard, defines neural networks and other data-mining models so that compliant tools can exchange them without vendor lock-in. A user can train a model in one vendor's application and then visualize, analyze, or evaluate it in another's. PMML producers and consumers include R (via the pmml package), SAS Enterprise Miner, SPSS, and STATISTICA.

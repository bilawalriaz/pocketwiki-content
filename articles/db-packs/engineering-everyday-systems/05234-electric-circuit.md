# Electric circuit

An electrical network is an interconnection of electrical components, such as batteries, resistors, inductors, capacitors, switches, and transistors, or a model of such an interconnection built from idealised elements like voltage sources, current sources, resistances, inductances, and capacitances. An electrical circuit is a network that forms a closed loop, giving current a return path. Every circuit is a network, but a network without a closed loop is an open circuit, not a circuit.

A resistive network contains only resistors and ideal current or voltage sources, which makes it easier to analyse than networks that include capacitors and inductors. When the sources are constant, the network is a DC network. The behaviour of arbitrary resistor networks can be predicted from their graph and geometric properties. A network that contains active electronic components, such as transistors, is an electronic circuit. Electronic circuits are usually nonlinear and need more sophisticated design and analysis tools than resistive networks.

## Classifying networks

Networks are sorted along three axes: passivity, linearity, and lumpiness. The first asks where the energy comes from. An active network contains at least one voltage source or current source that can deliver energy indefinitely; batteries and generators are practical examples. Active elements can inject power, provide power gain, and steer current flow. A passive network contains no source of electromotive force, only elements such as resistors and capacitors that absorb or store energy.

The second asks whether the network obeys superposition. A linear network contains only sources, linear lumped elements (resistors, capacitors, inductors), and linear distributed elements such as transmission lines. Signals in a linear network are superimposable, so the response to several inputs equals the sum of the responses to each input alone. This property allows analysis with frequency-domain methods, especially the Laplace transform, to obtain DC response, AC response, and transient response. Passive networks are usually taken to be linear, but an inductor with an iron core can be driven into saturation by a large enough current, after which its behaviour is very non-linear.

The third asks how the model represents component properties. Discrete resistors, capacitors, and inductors are lumped elements, with all of their resistance, capacitance, or inductance assumed to be concentrated at one place. The lumped-element model is the standard approach to circuit design. It fails at high frequencies or over long distances, such as power transmission lines, where a significant fraction of a wavelength fits across a component. The distributed-element model is used in those cases, and a design that mixes both is called semi-lumped; the combline filter is an example.

## Sources

Sources are classified as independent or dependent. An ideal independent source delivers the same voltage or current regardless of the rest of the circuit, with a value that is either constant (DC) or sinusoidal (AC). A dependent source delivers power, voltage, or current that depends on another element of the circuit, such as a voltage or current elsewhere in the network.

## Laws for linear resistive networks

A small set of laws describes every linear resistive network. Kirchhoff's current law states that the sum of currents entering a node equals the sum leaving it. Kirchhoff's voltage law states that the directed sum of potential differences around any loop is zero. Ohm's law states that the voltage across a resistor equals the resistance multiplied by the current through it. Norton's theorem says any network of sources and resistors is equivalent to an ideal current source in parallel with a single resistor. Thévenin's theorem gives the dual result: any such network is equivalent to a single voltage source in series with a single resistor. The superposition theorem says that in a linear network with several independent sources, the response in any branch is the sum of the responses computed with one source active at a time.

Applying these laws produces simultaneous equations that can be solved algebraically or numerically. They extend to networks containing reactances, the frequency-dependent opposition to current offered by capacitors and inductors, but they do not apply to networks with nonlinear or time-varying components.

## Design and simulation

To design any circuit, analog or digital, an engineer must predict the voltages and currents everywhere in it. Simple linear circuits can be analysed by hand using complex number theory. More complex circuits call for computer tools. Simulators such as SPICE and GNUCAP perform numerical analysis, while tools such as SapWin perform symbolic analysis. Hardware description languages such as VHDL-AMS and Verilog-AMS let engineers describe circuits for simulation, avoiding the time, cost, and risk of building physical prototypes.

Two numerical strategies dominate. In linearization around an operating point, the simulator first finds a steady state in which every node obeys Kirchhoff's current law and every element obeys its own voltage-current equation. It then replaces each nonlinear element with its small-signal linear approximation around that operating point, an application of Ohm's law, and solves the resulting linear system, typically by Gaussian elimination. In piecewise-linear approximation, used by tools such as the PLECS interface to Simulink, every nonlinear element is replaced by a network of ideal diodes that switches configuration whenever a diode turns on or off, and the circuit is then treated as fully linear. Refining the approximation increases accuracy at the cost of longer run times.

Source: adapted from "Electric circuit" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Electric_circuit

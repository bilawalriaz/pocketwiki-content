# LIDA (cognitive architecture)

LIDA is a hybrid cognitive architecture developed primarily by Stan Franklin and colleagues at the University of Memphis. Its goal is to model a broad spectrum of cognition in biological systems, from low-level perception and action to high-level reasoning. LIDA is empirically grounded in cognitive science and cognitive neuroscience, extends an earlier system called IDA by adding learning mechanisms, and serves three purposes: generating hypotheses for research, supplying control structures for software agents and robots, and giving thinkers a vocabulary for how minds work.

Two hypotheses define LIDA. First, much of human cognition works through frequently iterated interactions, called cognitive cycles, between conscious contents, various memory systems, and action selection; these cycles run at roughly 10 Hz. Second, cognitive cycles are the "atoms" of cognition, the building blocks from which higher-level processes are composed.

LIDA is hybrid because it is neither purely symbolic (rule-based on explicit symbols) nor purely connectionist (based on networks of simple neuron-like units). It borrows computational mechanisms chosen for their psychological plausibility rather than for uniformity, including sparse distributed memory, a schema mechanism, the Behavior Net, and Brooks's subsumption architecture. It also implements parts of several psychological theories, among them Global Workspace Theory, situated cognition, perceptual symbol systems, working memory, and long-term working memory.

A key design element is the codelet, which Franklin defines as a "special purpose, relatively independent, mini-agent typically implemented as a small piece of code running as a separate thread." Codelets handle small, specialised jobs in parallel, giving LIDA its distributed character.

## The Cognitive Cycle

Every cognitive cycle consists of three phases: understanding, consciousness, and action selection, the last of which includes learning.

In the understanding phase, incoming stimuli activate low-level feature detectors in sensory memory. Their output engages perceptual associative memory, whose higher-level feature detectors identify more abstract entities such as objects, categories, actions, and events. The resulting percept enters the Workspace, where it cues Transient Episodic Memory and Declarative Memory to produce local associations. These associations combine with the percept into a current situational model, the agent's best account of what is happening right now.

In the consciousness phase, attention codelets select portions of the situational model and form coalitions that compete for entry into the Global Workspace. The winning coalition becomes the content of consciousness and is broadcast globally across the system.

In the action selection and learning phase, the global broadcast reaches perceptual, episodic, and procedural memory, where it can create new entities and associations or reinforce old ones. In parallel, possible action schemes are instantiated from Procedural Memory and compete in Action Selection; the chosen behaviour triggers sensory-motor memory to produce the algorithm that runs it, completing the cycle. Each completed cycle is a cognitive "moment," and the continuous repetition of these moments is what makes higher-level thought possible.

## Origins and Lineage

LIDA grew out of three earlier systems. The first, Virtual Mattie (V-Mattie), was a software agent that gathered information from seminar organisers, composed weekly announcements, and mailed them to a list it maintained without human supervision. Adding a Global Workspace Theory–style consciousness mechanism to V-Mattie produced Conscious Mattie, the first software agent that was functionally, though not phenomenally, conscious.

Conscious Mattie in turn gave rise to IDA (Intelligent Distribution Agent), built for the US Navy. The Navy assigns sailors to new billets at the end of each tour, a process called distribution, carried out by almost 300 full-time detailers. IDA was designed to automate that role, was tested by former detailers, accepted by the Navy, and supported by Navy agencies with funding on the order of $1,500,000.

LIDA (Learning IDA) began as IDA augmented with several styles and modes of learning and has since grown into a much larger, generic software framework used for both research and as a basis for further agent and robotic control systems.

Source: adapted from "LIDA (cognitive architecture)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/LIDA_%28cognitive_architecture%29

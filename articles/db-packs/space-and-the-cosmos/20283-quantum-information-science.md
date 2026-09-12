# Quantum information science

Quantum information science studies how quantum systems can store, process, and transmit information. It combines quantum mechanics, information theory, and computer science, and covers both the limits of what is possible in principle and the engineering needed to build hardware.

The shift from classical to quantum information rests on two resources with no classical equivalent. A classical bit is 0 or 1; a qubit (quantum bit) lives in a superposition of both, so it can represent many states at once. Qubits can also be entangled, linked so that measuring one determines the state of another, no matter the distance.

## Hardware and engineering

Quantum information science is interdisciplinary by necessity: physics supplies the phenomena, computer science supplies the algorithms, mathematics supplies the proofs, and engineering supplies the devices. Google and IBM have driven hardware progress since the 2010s, and current machines exceed 100 qubits. Error rates remain high because of decoherence (the loss of quantum behaviour as a system interacts with its environment), unsuitable materials, and the difficulty of scaling.

Quantum cryptography devices are the first commercial result. The one-time pad, a Cold War spy cipher, encrypts messages with a random key used only once. Quantum entanglement can distribute that key securely: the no-cloning theorem forbids copying an unknown quantum state, and any eavesdropper disturbs the particles, so interception is detectable.

## Software and algorithms

Quantum programming languages such as Qiskit, Cirq, and Q# exist, though few skills transfer from classical programming. OpenQASM (Open Quantum Assembly Language) is a machine-independent language that describes quantum circuits as ordered sequences of gates, measurements, resets, and real-time classical computations, useful for implementing algorithms and debugging processors.

The field's signature algorithmic result is Peter Shor's 1994 prime factorisation algorithm. A fault-tolerant quantum computer with roughly 4,000 logical qubits could break widely used ciphers like RSA and ECC. This threat has spurred investment in post-quantum cryptography, classical algorithms designed to remain secure once large quantum computers arrive.

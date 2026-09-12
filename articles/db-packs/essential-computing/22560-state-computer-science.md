# State (computer science)

In information technology and computer science, a system is **stateful** when it is designed to remember preceding events or user interactions; the remembered information is called the **state** of the system. The set of all configurations a system can occupy is its **state space**, countable and often finite in a discrete system. Discrete behaviour consists of individually occurring actions (accepting input, producing output) that may or may not cause a transition to a new state. Digital logic circuits, automata, computer programs, and full computers are all stateful systems in this sense, and for any deterministic system the output at a given moment is completely determined by the current inputs together with the current state.

## Digital logic circuits

Digital logic comes in two types. **Combinational logic** produces outputs that depend solely on present inputs. **Sequential logic** produces outputs that are a function of both current inputs and the past history of inputs; that history is held in memory elements such as **flip-flops**. The combined contents of those memory elements, at a given instant, is the circuit's state, and it contains everything about prior inputs that the circuit can still see. Each binary memory element holds one of two values (0 or 1), so with N binary memory elements the circuit has at most 2^N distinct states.

## Program state

A computer program stores data in **variables**, named locations in memory, and the contents of those locations at a given instant during execution form the program's state.

For programs that process **streams of data** one item at a time, such as parsers, firewalls, communication protocols, and encryption, the terminology sharpens. When the program remembers information about earlier items in order to influence processing of the current item, it is a **stateful protocol**, and the data carried over from one cycle to the next is its state. When each item is processed independently from a clean slate, it is a **stateless protocol**.

Programming paradigms expose and manage state in different ways. **Imperative programming** describes computation in terms of the program state and the statements that change it; changes are implicit and managed by the runtime, so a subroutine can observe changes made elsewhere, a phenomenon known as **side effects**. **Object-oriented programming** limits that exposure by **encapsulating** state with the behaviour that acts on it inside **objects**; the state concealed this way is the object's **internal state**, and the practice reduces **coupling** between objects. **Declarative programming** describes desired results without specifying state changes directly. In **functional programming**, state is usually explicit: each step is modelled as a state variable passed into a state-transforming function, which returns the updated state as part of its result; a **pure** subroutine sees only the state variables within its own scope.

## Finite-state machines

Because the output of a sequential circuit or program at any moment is fully determined by its current inputs and current state, and because N binary memory elements bound the number of states at 2^N, the notion of state lends itself to an abstract model of computation: the **finite-state machine**, used to design both sequential digital circuits and the programs that imitate them.

## Examples

A television set is a stateful everyday device. Its digital tuner must remember the number of the **current channel** in order to compute the next channel when the user presses channel-up or channel-down; the result is stored back as the current channel. The set also stores a **volume** level that the volume buttons increment or decrement. Both numbers are part of the TV's state and are kept in **non-volatile memory**, so when the set is powered off and on again it resumes the previous station and volume.

A personal computer illustrates state at a larger scale: the state of the machine is the contents of all its memory elements. When a laptop enters **hibernation** to save energy, the state of the processor, memory, and I/O devices is written to the hard disk; on resume the state is restored and the processor continues from where it stopped.

Source: adapted from "State (computer science)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/State_%28computer_science%29

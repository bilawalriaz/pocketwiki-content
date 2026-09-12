# Cognitive robotics

Cognitive robotics is the subfield of robotics that tries to give a robot intelligent behaviour by giving it a processing architecture capable of learning and reasoning about how to act toward complex goals in a complex world. It is the engineering counterpart of embodied cognitive science and embodied embedded cognition, and in practice it pulls together robotic process automation, artificial intelligence, machine learning, deep learning, optical character recognition, image processing, process mining, analytics, software development, and system integration. The defining test is that the robot must be able to act in the real world, or, for simulated work, a virtual one.

## Why symbolic coding is the central problem

Classical cognitive modelling relied on translating the world into symbolic representations, but that translation has proven problematic, often untenable. Perception, action, and the meaning of a "symbol" are therefore the core issues the field has to solve: a cognitive robot must connect raw sensing and motor output to whatever internal representation it uses to plan and reason.

## Starting point: cognition as a template

Cognitive robotics takes human or animal cognition as its starting point rather than relying on traditional artificial intelligence techniques. Target capabilities drawn from that template include perception processing, attention allocation, anticipation, planning, complex motor coordination, reasoning about other agents, and reasoning about one's own mental states.

## How the robot learns

Three techniques dominate the learning side of the field, in order of increasing autonomy.

**Motor babbling.** The robot executes pseudo-random complex motor movements and correlates them with resulting visual or auditory feedback. From these correlations it builds expectations about what sensory feedback should follow a given motor pattern, and can then run the mapping backwards: desired feedback selects a motor command. This is thought to be analogous to how a baby learns to reach for objects or produce speech sounds. For simpler systems where inverse kinematics already converts a desired result into motor output, this step can be skipped.

**Imitation.** Once a robot can coordinate its motors to produce a desired result, it can watch another agent and attempt to reproduce the performance. The hard part is converting what is seen in a complex scene into a motor plan for the imitating robot. Imitation is a high-level cognitive behaviour and is not strictly required in a basic model of embodied animal cognition.

**Autonomous knowledge acquisition.** The robot explores the environment on its own, guided by an internal system of goals and beliefs. More directed exploration uses curiosity algorithms such as Intelligent Adaptive Curiosity and Category-Based Intrinsic Motivation. These break sensory input into a finite set of categories and attach a predictor, often an artificial neural network, to each. The predictor tracks its own error over time, and the robot preferentially explores the categories where prediction error is falling fastest, treating that reduction as learning.

## Other architectures

Some researchers build on highly modular symbol-processing cognitive architectures such as ACT-R and Soar, which have been used to simulate operator and human performance on simplified, symbolic laboratory data. The open problem is extending those architectures to handle real-world sensory input as it unfolds through time, which requires translating the world into symbols and the relationships between them.

## Open questions

Two fundamental questions remain unsettled. First, how much human programming should, or can, support the learning processes at all. Second, how should progress be quantified, and what forms of reward and punishment are effective for a robot, given that the analogies to candy or encouragement used with children do not transfer directly.

Source: adapted from "Cognitive robotics" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Cognitive_robotics

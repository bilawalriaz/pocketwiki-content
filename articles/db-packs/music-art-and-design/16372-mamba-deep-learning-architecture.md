# Mamba (deep learning architecture)

Mamba is a deep learning architecture for sequence modeling, introduced by Albert Gu (Carnegie Mellon University) and Tri Dao (Princeton University) in a paper presented at the First Conference on Language Modeling on 10 July 2024. It was built to address limitations of transformer models, especially their difficulty with long sequences, and extends an earlier architecture called the Structured State Space sequence model (S4).

## The foundation: S4

To handle long sequences efficiently, Mamba builds on S4, a structured state space model. A state space model describes how a hidden state evolves over time and produces outputs; "structured" means the matrices governing that evolution are restricted to special forms that are fast to compute. S4 combines three strengths:

- Continuous-time models, which let it accept irregularly sampled data.
- Recurrent models, which give an effectively unbounded context.
- Convolutional models, which allow training to be parallelized on hardware like GPUs.

The result is a layer that captures long-range dependencies while remaining computationally efficient in both training and inference.

## What Mamba adds

Mamba keeps S4's core but makes the SSM parameters depend on the input. Where S4 used a time-invariant system with the same transition dynamics for every token, Mamba uses a time-varying one whose parameters are computed from the current input. This selection mechanism lets the model amplify or suppress different inputs, filtering which information is worth remembering and which can be discarded.

The cost of this flexibility is that the parameters change at every step, which breaks the convolutional trick that made S4 easy to parallelize. Mamba recovers efficiency with a hardware-aware algorithm that runs well on modern GPUs through:

- Kernel fusion, combining several operations into a single GPU pass.
- Parallel scan, computing the recurrence across a sequence in parallel rather than step by step.
- Recomputation, trading extra arithmetic for lower memory by avoiding materializing large intermediate states.

The implementation never materializes the expanded state in memory-intensive layers, keeping memory and compute usage low. Mamba also folds the SSM block into an otherwise standard design alongside multilayer perceptron (MLP) blocks (small fully connected feedforward networks), producing a homogeneous stack that works across language, audio, and genomics.

## A notable variant

MoE-Mamba interleaves standard Mamba layers with mixture-of-experts (MoE) layers. A mixture-of-experts layer routes each token to a small subset of specialized sub-networks rather than running every parameter on every token, increasing capacity without proportional compute cost. MoE-Mamba reaches Mamba's quality with about 2.2× fewer training steps while retaining Mamba's inference-speed advantage over transformers, because each token still sees the full sequence context before the MoE step selects which experts to apply.

## Position in the landscape

Mamba sits among a growing set of architectures positioned as alternatives to transformers for long-sequence tasks. Its practical contribution is demonstrating that a selectively time-varying SSM, paired with hardware-aware kernels, can process long sequences more efficiently than earlier methods while keeping a simple, homogeneous structure that generalizes across data types.

Source: adapted from "Mamba (deep learning architecture)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Mamba_%28deep_learning_architecture%29

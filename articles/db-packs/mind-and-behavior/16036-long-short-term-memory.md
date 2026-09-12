# Long short-term memory

Long short-term memory (LSTM) is a recurrent neural network (RNN) architecture designed to mitigate the vanishing gradient problem, which prevents ordinary RNNs from learning dependencies across more than a few time steps. During backpropagation, gradients in a plain RNN shrink toward zero across long sequences, so the network stops adjusting weights that connect distant events. An LSTM can preserve useful signals across thousands of timesteps, giving it a relative insensitivity to gap length that hidden Markov models and standard RNNs lack. The name borrows the long-term and short-term memory analogy from cognitive psychology.

## Core idea

An LSTM unit processes one input at a time while carrying a separate cell state, a running memory, alongside the usual hidden state. Three learned gates control how that memory is updated and read. Each gate looks at the current input and the previous hidden state, then outputs a vector of numbers between 0 and 1 that is applied element-wise to the cell state through the Hadamard product. The cell state acts as a continuous conveyor belt that can be partly retained, partly overwritten, and partly exposed, while the hidden state is what the rest of the network actually sees at each step.

## The three gates

- Forget gate f_t: decides what to discard from the previous cell state. Values near 1 keep the corresponding memory; values near 0 erase it.
- Input gate i_t: decides which new candidate information to write into the cell state. Its companion candidate vector c̃_t proposes the new content.
- Output gate o_t: decides which parts of the cell state to expose as the hidden state h_t for the current step.

The cell update is c_t = f_t ⊙ c_{t-1} + i_t ⊙ c̃_t: old memory is filtered by forgetting, and new information is filtered by the input gate before being added. The hidden output is h_t = o_t ⊙ σ_h(c_t). Because memory can pass through many steps with mild, learned multiplicative scaling, gradients do not vanish as quickly as in a plain RNN, though they can still explode.

## Equations of the standard LSTM

With x_t the input, h_{t-1} the previous hidden state, c_{t-1} the previous cell state, W and U learned weight matrices, b bias vectors, σ_g the sigmoid, and σ_c the hyperbolic tangent:

```
f_t = σ_g(W_f x_t + U_f h_{t-1} + b_f)
i_t = σ_g(W_i x_t + U_i h_{t-1} + b_i)
o_t = σ_g(W_o x_t + U_o h_{t-1} + b_o)
c̃_t = σ_c(W_c x_t + U_c h_{t-1} + b_c)
c_t = f_t ⊙ c_{t-1} + i_t ⊙ c̃_t
h_t = o_t ⊙ σ_h(c_t)
```

Initial values are c_0 = 0 and h_0 = 0. To interpret "Dave, as a result of his controversial claims, is now a pariah," the network must remember that "Dave" is singular and masculine long enough to match "his," then release that information after the verb "is." The forget and output gates learn to carry those grammatical features forward and drop them when they are no longer relevant.

## Training

LSTMs are trained with gradient descent using backpropagation through time. Many applications stack multiple LSTM layers and optimize them with Connectionist Temporal Classification (CTC), which learns both the alignment between input and output sequences and the labels themselves without pre-segmented training data. When no labeled signal exists, LSTM weights can instead be optimized by neuroevolution or policy gradient methods. Gradient clipping is standard practice because LSTMs remain vulnerable to exploding gradients.

## Variants

- Peephole LSTM (2000): the gates look directly at c_{t-1} instead of h_{t-1}, accessing the running memory at the moment of deciding.
- Peephole convolutional LSTM: replaces matrix multiplications with convolutions, so the architecture can process spatial data such as video frames while keeping the same gating.
- Bidirectional LSTM: runs the sequence forward and backward and concatenates the two hidden states, giving each step access to both past and future context.
- Gated recurrent unit (GRU), published by Cho et al. in 2014: merges the cell and hidden state and reduces three gates to two (reset and update).
- Highway network (2015) and xLSTM (2024): later architectures that build on LSTM gating, with xLSTM adding blocks parallelizable like Transformers while retaining state tracking.

On very large text corpora, Transformers have been shown to scale better than LSTM, as Kaplan et al. reported in 2020.

## Brief history

Sepp Hochreiter's 1991 diploma thesis identified the vanishing gradient problem. Hochreiter and Jürgen Schmidhuber published the original LSTM in a 1995 technical report, at NIPS 1996, and in the 1997 Neural Computation paper that remains the standard reference; their initial design included input and output gates. Felix Gers, Schmidhuber, and Fred Cummins added the forget gate in 1999, giving the LSTM the ability to reset its own state and producing the version most widely used today, and they introduced peephole connections in 2000. In 2005 Graves and Schmidhuber published a fully backpropagated bidirectional LSTM, and in 2006 Graves, Fernández, Gomez, and Schmidhuber introduced CTC. Cho et al. proposed the GRU in 2014.

## Notable applications

Google deployed an LSTM trained with CTC for Google Voice transcription in 2015, cutting errors by 49 percent, and used LSTMs in Google Neural Machine Translation in 2016 to reduce translation errors by 60 percent. Facebook was performing roughly 4.5 billion LSTM-based automatic translations per day by 2017, and Microsoft reached 94.9 percent accuracy on the Switchboard speech corpus that year. Amazon's Polly uses a bidirectional LSTM for text-to-speech, and Apple integrated LSTMs into QuickType and Siri. OpenAI used LSTMs trained by policy gradients to beat humans at Dota 2 in 2018 and to control a dexterous robot hand, while DeepMind used LSTMs to reach Grandmaster level in StarCraft II in 2019. Other widespread uses include time-series forecasting, anomaly detection, machine translation, rhythm and music modeling, handwriting recognition, protein homology detection, traffic forecasting, and energy load prediction.

Source: adapted from "Long short-term memory" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Long_short-term_memory

# Deep learning

Deep learning is machine learning that uses neural networks with many layers, typically three to several hundred or thousand, to transform raw input into useful predictions. The adjective "deep" refers to the number of layers data passes through, not to any deeper understanding. Methods can be supervised, semi-supervised, or unsupervised.

## The central idea

A neural network is a chain of small mathematical functions, called artificial neurons, organized into layers. Each connection carries a numerical weight, and each neuron applies a nonlinear function to its weighted inputs. Signals flow from an input layer through one or more hidden layers to an output layer. Training adjusts the weights so outputs match desired answers on example data, using backpropagation, which is the chain rule from calculus applied repeatedly to compute how each weight should change.

The consequence of depth is compositional representation. In an image classifier, the first layer might detect edges, the second combines edges into shapes, the third assembles shapes into parts like eyes and noses, and a deeper layer recognizes a face. The network learns which features belong at which level by itself, replacing the hand-crafted feature engineering older machine learning required. More layers, beyond a point, do not add raw function-fitting power: a network only two layers deep can already approximate any continuous function, by the universal approximation theorem proved by George Cybenko in 1989 for sigmoid activations and generalized by Kurt Hornik in 1991. The advantage of depth is that it builds features useful for the data being learned, so a deep model outperforms a shallow one with the same number of parameters.

The chain of transformations from input to output is the credit assignment path, or CAP. For a feedforward network its depth equals the number of hidden layers plus one. For a recurrent network, where signals cycle, the CAP can be effectively unlimited. No exact threshold separates "shallow" from "deep," but most researchers take CAP depth greater than two as deep.

## Common architectures

- **Fully connected (feedforward) networks**: every neuron in one layer connects to every neuron in the next. A general-purpose default.
- **Convolutional neural networks (CNNs)**: shared weights and pooling detect local patterns, dominant in image and video tasks.
- **Recurrent neural networks (RNNs)**: feed outputs back as inputs, suited to sequences. Long short-term memory (LSTM), introduced by Sepp Hochreiter and Jürgen Schmidhuber in 1995 with a "forget gate" added in 1999, addresses the vanishing-gradient problem and can learn dependencies across thousands of time steps.
- **Generative adversarial networks (GANs)**: a generator and a discriminator contest each other.
- **Transformers**: process sequences in parallel using attention, the basis of modern language models.
- **Deep belief networks and deep Boltzmann machines**: layered generative models trainable without labels.

## How training works

Training is dominated by stochastic gradient descent: compute the prediction error on a small batch, use backpropagation to find the gradient of the error with respect to every weight, take a small step in the direction that reduces error, and repeat. Modern stochastic gradient descent traces to Shun'ichi Amari's 1967 multilayer perceptron experiments. Backpropagation in its modern form was derived by Seppo Linnainmaa in 1970, applied to neural networks by Paul Werbos in 1982, and popularized by David Rumelhart and colleagues in 1986.

A practical challenge is overfitting: deep networks can memorize training data at the expense of generalization. Common countermeasures include weight decay (ℓ2 or ℓ1 regularization), dropout, which randomly omits units during training, and data augmentation.

## A brief history

The first working deep-learning algorithm was the Group Method of Data Handling, published by Alexey Ivakhnenko and Lapa in 1965, which trained an eight-layer polynomial network layer by layer. The perceptron came from Frank Rosenblatt in 1958, the Ising model from Wilhelm Lenz and Ernst Ising in the 1920s, and the ReLU activation from Kunihiko Fukushima in 1969, the function that became the deep-learning default. The convolutional "neocognitron" appeared in 1979.

The 1980s brought backpropagation, the TDNN, and LeNet (Yann LeCun, 1989) for handwritten-digit recognition. The 1990s were a comparative lull: hand-crafted systems such as Gaussian-mixture and hidden-Markov models dominated speech, while simpler classifiers like support vector machines were preferred for many tasks. Deep neural networks reached industry first in check-reading: by the early 2000s LeNet-derived CNNs processed an estimated 10–20% of all US checks.

The 2010s "deep learning revolution" was driven mainly by GPU hardware. A 2009 demonstration by Raina, Madhavan, and Andrew Ng trained a 100-million-parameter deep belief network on 30 Nvidia GTX 280 GPUs, up to 70 times faster than CPUs. DanNet (2011) achieved superhuman visual pattern recognition, and AlexNet (Krizhevsky, Sutskever, Hinton, 2012) won ImageNet by a large margin. ResNet (2015) enabled training of networks with hundreds of layers. GANs drove image generation through 2014–2018, after which diffusion models such as DALL·E 2 and Stable Diffusion (2022) eclipsed them. Yoshua Bengio, Geoffrey Hinton, and Yann LeCun received the 2018 Turing Award for the underlying breakthroughs.

## Hardware

Training a large deep network is dominated by dense matrix multiplications, which GPUs handle efficiently. By 2019 GPUs had replaced CPUs as the dominant training hardware for commercial cloud AI. OpenAI estimated a 300,000-fold increase in compute used by the largest deep-learning projects between AlexNet (2012) and AlphaZero (2017), doubling roughly every 3.4 months. Specialized chips followed: Google's tensor processing units (TPUs), Huawei's neural processing units (NPUs), and experimental photonic accelerators that perform trillions of multiply-accumulate operations per second through wavelength-division multiplexing.

## Applications and limits

Deep learning underpins automatic speech recognition in all major commercial systems, image classification reaching superhuman accuracy on traffic signs in 2011 and faces in 2014, machine translation including Google's LSTM-based system that handles over 100 languages, drug discovery (AtomNet for structure-based design, AlphaFold for protein structure prediction), medical image analysis, recommendation systems, materials science (Google DeepMind's GNoME discovered over 2 million candidate inorganic crystals in 2023), and weather forecasting (DeepMind's GraphCast predicts ten-day global weather in under a minute).

Two well-known failure modes motivate ongoing research. Adversarial examples show that small, often imperceptible perturbations to an image can flip a network's confident classification. Deep networks can also assign high confidence to inputs that look like nonsense to humans, reflecting the gap between their statistical pattern-matching and human reasoning.

Source: adapted from "Deep learning" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Deep_learning

# Neural network (machine learning)

A neural network is a computational model that learns patterns from data by adjusting the strengths of connections between simple numerical units. Inspired by biological neurons, it is in practice a statistical estimator: a multilayer system of weighted sums and nonlinear functions whose parameters are tuned to fit examples.

## What a single neuron does

Each artificial neuron takes one or more numerical inputs, multiplies each by a connection weight, sums them, adds a bias term, and passes the result through a nonlinear **activation function** to produce a single output. A common activation is **ReLU** (rectified linear unit), which simply outputs zero for negative inputs. Without nonlinearity, stacking layers collapses into a single linear model.

## How neurons are organised

Neurons are grouped into **layers**. The first layer, the **input layer**, receives raw data such as image pixels. The last layer, the **output layer**, produces the final answer. In between sit one or more **hidden layers**, each transforming its inputs. A network is called *deep* when it has at least two hidden layers, and each successive layer represents the data at a higher level of abstraction: raw pixels become edges, edges become shapes, shapes become objects.

Four structural families dominate. In a **feedforward network**, signals flow only forward and information is processed once per pass. A **recurrent neural network (RNN)** forms cycles that carry memory of past inputs, suiting it to sequences like speech. A **convolutional neural network (CNN)** connects each neuron to only a small region of the previous layer, exploiting locality and making it efficient for images. The **transformer** (2017) uses an *attention mechanism* that lets every position in a sequence look at every other position, at a cost that grows quadratically with context length. Transformers underpin modern large language models.

## How a network learns

Learning means adjusting connection weights so outputs match desired values. A **loss function** measures the gap between prediction and target; for regression, mean squared error is typical. Training uses **backpropagation**, an application of the chain rule that computes how much each weight contributed to the output error, then nudges each weight down the gradient. The **learning rate** sets the step size. **Stochastic gradient descent**, updating weights on small random batches, became the dominant method.

The **universal approximation theorem** states that a sufficiently wide multilayer network can approximate any continuous function to arbitrary accuracy, though it gives no recipe for finding the right weights. In practice training can stall in local minima or fail to generalise from training data to new inputs, a problem called **overfitting**, addressed by holding out a validation set and by regularisation. Training a modern large language model requires millions of examples and costs tens of millions of dollars.

## Learning paradigms

In **supervised learning**, each example is paired with a known answer. In **unsupervised learning**, only inputs are given and the network learns structure such as clusters or compressed representations. **Self-supervised learning** generates its own labels, for example by predicting the next word, and forms the pretraining stage of large language models. In **reinforcement learning**, an agent takes actions in an environment and learns from rewards, modelled as a Markov decision process over states and actions.

## Brief history

Linear models trace to Legendre (1805) and Gauss (1795), who used least-squares fitting for planetary motion. McCulloch and Pitts (1943) proposed a non-learning mathematical neuron capable of representing logical functions. Frank Rosenblatt's **perceptron** (1958) was the first implemented learning network, but the 1969 book *Perceptrons* by Minsky and Papert showed that single-layer perceptrons cannot learn XOR, deflating funding through the 1970s.

The first working deep learning algorithm was the group method of data handling (Ivakhnenko and Lapa, 1965), an eight-layer network trained layer by layer. Amari (1967) trained a five-layer multilayer perceptron with stochastic gradient descent. Backpropagation, published by Linnainmaa in 1970 and applied to neural networks by Werbos in 1982, was popularised by Rumelhart, Hinton, and Williams in 1986. Fukushima's 1979 **neocognitron** introduced the convolutional and max-pooling layers that define modern CNNs; LeNet-5 (LeCun, 1998) applied them to handwritten digits.

The modern era began with **AlexNet** (Krizhevsky, Sutskever, and Hinton, 2012), which won the ImageNet contest using GPU training. **Generative adversarial networks** (Goodfellow et al., 2014) pit a generator against a discriminator, and were later eclipsed by **diffusion models**, which underpin systems such as DALL·E 2 and Stable Diffusion. **Transformers** (Vaswani et al., 2017) replaced recurrence with attention and became the basis of modern large language models.

## Limitations and practical concerns

Neural networks are **black boxes** whose decisions are hard to interpret, and they are vulnerable to **adversarial examples**, small input perturbations that cause confident wrong predictions. They inherit training-data biases; a 2018 Amazon recruiting tool down-ranked résumés containing the word "women" because they were underrepresented in historical hires. Training is also computationally expensive: the human brain runs on about 20 watts, while training a modern transformer draws hundreds of megawatts. When input statistics shift after deployment, a phenomenon called **concept drift**, accuracy can degrade silently, so deployed models require ongoing monitoring.

Source: adapted from "Neural network (machine learning)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Neural_network_%28machine_learning%29

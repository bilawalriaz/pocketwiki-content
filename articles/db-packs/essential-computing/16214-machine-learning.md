# Machine learning

Machine learning (ML) is a field of artificial intelligence in which computers learn rules from data instead of being programmed with them. The term was coined in 1959 by IBM's Arthur Samuel, who built a checkers program that improved through play. Tom Mitchell later gave the standard working definition: a program learns from experience *E* with respect to tasks *T* measured by performance *P* if its performance at *T*, as measured by *P*, improves with *E*.

A learner starts with a mathematical model whose internal numbers (parameters) are wrong or random. It is shown many training examples, and an optimisation algorithm nudges the parameters to reduce a loss function, a number that measures how far the model's predictions are from the correct answers. Training repeats until the loss stops falling. The trained model is then tested on held-out examples it never saw, because the real goal is **generalisation**: performing accurately on new data drawn from the same underlying distribution, not memorising the training set.

## How a learner is shaped

Most learning falls into three paradigms, distinguished by what feedback the data provides.

- **Supervised learning.** Each example is an input paired with the correct output (a label). The learner infers a mapping from inputs to outputs. Classification assigns inputs to discrete categories (spam or not spam); regression predicts a number (a temperature, a price).
- **Unsupervised learning.** No labels are given. The learner must find structure on its own, usually by clustering similar points together or by reducing many correlated variables to a few.
- **Reinforcement learning.** An agent takes actions in an environment and receives rewards or penalties. It learns a policy, a rule for choosing actions, that maximises cumulative reward. DeepMind's AlphaGo (2016) used this approach with deep neural networks to defeat professional human Go players without handicaps.

Two further variants sit between these: **semi-supervised** learning uses mostly unlabelled data with a small labelled subset, and **self-supervised** learning generates its own labels from the data, for example predicting masked words in a sentence.

The central theoretical idea is **empirical risk minimisation**: most algorithms, from linear regression to deep networks, can be viewed as searching for parameters that minimise average loss on a training set. A related framework, **probably approximately correct (PAC) learning**, asks how many examples are needed to guarantee, with high probability, low error on new data.

## The fitting trap: bias and overfitting

A model that is too simple cannot capture the patterns in the data and **underfits**, leaving loss high on both training and test sets. A model that is too complex can **overfit**: it memorises training noise, so training loss falls to near zero but test loss rises. The **bias–variance tradeoff** captures this tension. Standard remedies include holding out a validation set, cross-validation, regularisation (penalising large parameters), and early stopping. The aim is to match model complexity to the amount and noisiness of the data.

## Common model families

- **Linear and logistic regression** fit a weighted sum of inputs; logistic regression handles classification by passing that sum through a sigmoid function that squashes any number into the range 0 to 1. A support vector machine draws the widest possible linear boundary between two classes, using a "kernel trick" to handle non-linear cases.
- **Decision trees** split the input space with yes/no questions; **random forests** average many trees trained on random data slices, reducing overfitting.
- **Artificial neural networks** connect many simple numeric units ("neurons") in layers. **Deep learning** stacks many such layers, letting the network build a hierarchy of features (edges, then shapes, then objects) from raw inputs. The 2012 AlexNet image classifier, which used graphics processing units (GPUs) to train, demonstrated that deep networks outperform previous methods on perceptual tasks and triggered the modern deep-learning era. The 2017 **Transformer** architecture, based on an attention mechanism that weights which input tokens to focus on, came to dominate language and is now the basis of large language models. **Generative adversarial networks** (2014) train two networks against each other to produce realistic synthetic data. The **Chinchilla 70B** model showed large language models can act as competitive lossless compressors on some data, though this may partly reflect overlap between the test data and the model's training set.
- **Bayesian networks** represent conditional dependencies among variables as a directed graph, letting the system reason under uncertainty.

## How ML sits among its neighbours

- **Statistics and ML** share many methods but differ in goal: statistics draws inferences about a population from a sample, while ML finds generalisable predictive patterns. Statistics traditionally fixes a model form in advance; ML lets the data shape the model.
- **Data mining** reuses ML methods, but its goal is discovering *previously unknown* properties in data, whereas ML typically aims to reproduce *known* properties.
- **Data compression** is mathematically equivalent to prediction: predicting the next symbol well is the same problem as compressing a stream well, which is why large language models can also compress text.
- **AI** is the broader goal of intelligent behaviour; ML is one approach to it, alongside symbolic reasoning. **Deep learning** is a subset of ML, which is a subset of AI.

## Training requires honest data

ML models are only as good as their training data. A model trained on past hospital admissions may learn to replicate racial or gender bias; a resume screener trained on a firm's historical hires may encode that firm's discrimination. **Algorithmic bias** arises when training data is unrepresentative or reflects historical prejudice, and is now treated as a central engineering concern alongside accuracy. Federated learning, used by Google's Gboard, trains a model across many user devices without sending raw data to a central server, preserving privacy.

## Failure modes and limits

ML systems fail in distinctive ways. The **black-box problem** is that even their designers cannot always explain a particular prediction, which has legal and ethical consequences when systems affect jobs, loans, or sentencing. **Adversarial examples** are tiny, often imperceptible pixel changes that flip a classifier's answer. **Model collapse**, sometimes called "AI inbreeding", degrades a model trained on outputs from previous generative models. **Hallucinations** are plausible-sounding but false statements produced by large language models, such as fabricated citations.

A model is also limited by what it can *learn*: an image classifier trained only on brown horses and black cats may learn to associate brown patches with horses, the wrong feature. Real-world classifiers sometimes rely on pixel correlations humans do not perceive, and altering those correlations can produce "adversarial" images that fool the system.

Source: adapted from "Machine learning" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Machine_learning

# Deep belief network

A deep belief network (DBN) is a generative deep neural network built by stacking simpler unsupervised modules, one on top of another. Each module learns to represent its inputs, and the stack of these representations gives the network its "depth." Once pretrained without labels, a DBN can be fine-tuned with labelled data to classify inputs, which is why it counts as one of the first practical deep learning models.

## Architecture

A DBN has multiple layers of latent variables, often called hidden units. Connections run only between adjacent layers; units within the same layer do not connect to each other.

Each sub-network is typically a restricted Boltzmann machine (RBM): an undirected, energy-based model with one visible layer and one hidden layer, again with no intra-layer connections. The energy function E(v, h) assigns a scalar score to every joint configuration of visible and hidden units, and the probability of a visible vector is

p(v) = (1/Z) Σₕ exp(−E(v, h)),

where Z is the partition function that normalises over all configurations. A trained RBM assigns low energy to configurations resembling the training data and high energy to others. Because there are no within-layer connections, inference is simple: given one layer, the units of the other are conditionally independent and can be updated in parallel.

## Unsupervised pretraining, layer by layer

A DBN is trained one module at a time, starting from the bottom. This greedy, layer-wise procedure was the key insight that made deep learning work, since optimising a deep network end-to-end was previously infeasible.

The training algorithm for each RBM is contrastive divergence (CD), introduced by Geoffrey Hinton. CD is a fast approximation to maximum likelihood. The gradient of log p(v) with respect to a weight wᵢⱼ has the form ⟨vᵢhⱼ⟩_data − ⟨vᵢhⱼ⟩_model, where ⟨·⟩_p denotes an average under distribution p. The first term is computed by clamping a training example on the visible units; the second term normally requires long runs of alternating Gibbs sampling. CD replaces it with just n steps of Gibbs sampling starting from the data, with n = 1 often working well. The procedure is:

1. Set the visible units to a training vector.
2. Update all hidden units in parallel from the visible units using p(hⱼ = 1 | V) = σ(bⱼ + Σᵢ vᵢwᵢⱼ), where σ is the sigmoid and bⱼ is the hidden bias.
3. Update all visible units in parallel from the hidden units using p(vᵢ = 1 | H) = σ(aᵢ + Σⱼ hⱼwᵢⱼ), where aᵢ is the visible bias. This step is the "reconstruction."
4. Re-update the hidden units from the reconstructed visibles using the same rule as step 2.
5. Apply the weight update Δwᵢⱼ ∝ ⟨vᵢhⱼ⟩_data − ⟨vᵢhⱼ⟩_reconstruction.

Although CD does not follow the gradient of any function, so the approximation to maximum likelihood is crude, it is empirically effective.

Once the bottom RBM is trained, a new RBM is stacked on top. Its visible layer takes input from the hidden activations of the layer below and is trained with the same CD procedure. This repeats until the desired depth is reached, and each layer ends up acting as a feature detector for the representation beneath it.

## Supervised fine-tuning

After pretraining, the DBN can be further trained with labelled data to perform classification, with the pretrained weights acting as the starting point.

## Applications

DBNs have been applied to electroencephalography analysis and to drug discovery tasks such as quantitative structure–activity relationship (QSAR) modelling, where learning useful molecular representations from unlabelled data is valuable.

Source: adapted from "Deep belief network" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Deep_belief_network

# Active learning (machine learning)

Active learning is a machine learning approach in which the algorithm itself selects which unlabelled examples to send for labelling, rather than passively receiving a pre-labelled set. Labels come from a human expert, a crowd, or another information source called a teacher or oracle. In statistics this is sometimes called optimal experimental design.

Unlabelled data is usually abundant, but manual labelling is slow and expensive because the teacher must be a domain expert who can consult authoritative sources when uncertain. By asking for labels only on the examples it expects to learn the most from, the learner can reach a given accuracy with far fewer labels than ordinary supervised learning requires. The risk is that a poorly chosen query strategy wastes effort on uninformative examples, or gets overwhelmed by them. Active learning has been extended to multi-label problems, hybrid active–passive settings, and online (single-pass) settings that combine machine learning concepts such as conflict and ignorance with adaptive policies from online learning. Large projects can use crowdsourcing platforms such as Amazon Mechanical Turk to put many humans in the loop.

## The iteration

Each round splits the data set T into three subsets: T_K,i holds examples whose label is already known, T_U,i holds the unlabelled examples, and T_C,i is the subset chosen from T_U,i to be sent to the teacher that round. Most active learning research concerns how to pick T_C,i well.

## Scenarios

Three settings dominate.

**Pool-based sampling.** The learner has access to a large pool of unlabelled instances and scores them all, typically by training a probabilistic model such as logistic regression or an SVM on the currently labelled subset. It asks the teacher to label the instances it is least confident about. In theory this requires holding the whole pool in memory, but in practice the bottleneck is the cost of the human expert's time, not memory.

**Stream-based selective sampling.** Unlabelled instances arrive one at a time, and the learner decides for each whether to request its label or skip it. Without a global view of the pool, the early decisions are weaker, and the teacher usually labels more examples than in the pool-based case.

**Membership query synthesis.** The learner generates its own candidate inputs from an underlying distribution and asks the teacher to label them, such as clipping a picture to show only a leg and asking whether it belongs to a human or an animal. Synthesis is attractive for small data sets, but the inputs must obey the same constraints as real ones. As features and their dependencies grow, generating realistic synthetic data becomes very hard; laboratory values illustrate this, since the components of a white blood cell differential are percentages and must sum to 100.

## Query strategies

The main families of selection rule are:

- Uncertainty sampling: label the points the current model is least sure about.
- Query by committee: train several models on the labelled data and label the points on which they disagree most.
- Expected model change: label the points that would alter the current model the most.
- Expected error reduction: label the points expected to lower generalisation error the most.
- Variance reduction: label the points that would cut the model's output variance.
- Balance of exploration and exploitation, for example Active Thompson Sampling, which places a sampling distribution over the pool each round and queries the point drawn from it, treating the choice as a contextual bandit problem. Exponentiated Gradient Exploration adds an optimal amount of random exploration on top of any active learning algorithm.
- Conformal prediction: label points whose predicted similarity to existing labelled examples is weak, since weak similarity implies low prediction confidence.
- Diversity-based selection, including querying from diverse subspaces or partitions in a tree model, and mismatch-first farthest-traversal, which first targets wrongly predicted points and then spreads remaining queries as far apart as possible.
- User-centred labelling, where dimensionality reduction is applied to graphs and scatter plots and the user labels the compiled points.

It is hard to predict in advance which strategy fits a given problem, which has motivated meta-learning approaches that learn the strategy itself.

## SVM-based selection: minimum marginal hyperplane

Support-vector machines give a natural selection rule. Each unlabelled point has a margin W, its distance to the SVM's separating hyperplane. Points with the smallest W are the ones the SVM is most uncertain about, so they are the natural candidates for labelling. Symmetric variants pick the largest margins, and trade-off methods mix the two.

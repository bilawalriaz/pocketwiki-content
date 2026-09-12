# Decision tree learning

A decision tree is a flowchart for prediction. Each internal node tests a feature ("is age < 9.5?"), each branch follows an answer, and each leaf gives a prediction. To classify a new case, you walk from the root down the path that matches its features until you hit a leaf.

When the leaf predicts a class label, the tree is a classification tree; when it predicts a number, it is a regression tree. The umbrella term for both is CART, introduced by Breiman et al. in 1984. The Titanic survival tree in the source is a small example: it splits passengers first by sex, then by age and number of siblings, and its leaves give the probability of survival for each subgroup.

## Building a tree

The learning algorithm is top-down induction of decision trees (TDIDT), a greedy procedure. Start with all training data at the root, pick the feature whose split produces the purest children, split, and recurse on each child until a node contains only one class or further splitting stops helping. Greedy here means the algorithm commits to the locally best split at every step and never reconsiders it, which is fast but not guaranteed to find the globally optimal tree. The result is a "white box" model: every prediction can be explained by the Boolean conditions along one path, unlike a neural network.

Because splits are chosen greedily and trees can grow until every leaf is pure, a fully grown tree often memorises noise. Pruning trims branches that hurt accuracy on held-out data, and the recursion stops early when a split no longer adds value. Information gain favours features with many possible values, so C4.5 uses an information gain ratio instead, and the Conditional Inference approach replaces the splitting criterion with non-parametric significance tests, which removes that bias and the need for pruning.

## How a split is judged

The most common criteria are:

- Gini impurity, used by CART. It is the probability that a randomly chosen element in a node would be mislabelled if labelled by the node's class distribution. It is zero when the node is pure and equals 1 − Σ pᵢ².
- Information gain, used by ID3, C4.5, and C5.0. It is the drop in Shannon entropy between the parent node and the weighted sum of its children, with H(T) = −Σ pᵢ log₂ pᵢ. The split with the highest gain is chosen.
- Variance reduction, used for regression trees. It is the drop in variance of the target value across the split and works directly on continuous targets.
- Estimate of Positive Correctness, a simple score of true positives minus false positives, and the related true positive rate from the confusion matrix, which accounts for the proportion of positives.

For example, a 14-row dataset of "play" (yes or no) with features outlook, temperature, humidity, and windy has parent entropy H([9, 5]) = 0.94 bits. Splitting on windy gives a windy-true child with three yes and three no (entropy 1.0) and a windy-false child with six yes and two no (entropy 0.81), so the weighted post-split entropy is about 0.89, yielding an information gain of 0.05 bits for that feature. The algorithm compares this against the gain from splitting on the other three features and picks the highest.

## Ensembles and variants

A single greedy tree is high-variance, since small changes in the training data can flip the splits. Ensembles reduce this by growing many trees and combining their votes. Bagging (bootstrap aggregating) trains each tree on a different resample of the data, then averages votes. Random forests add a second randomisation, restricting each split to a random subset of features, which decorrelates the trees. Boosted trees such as AdaBoost train trees one at a time, weighting previously misclassified examples more heavily. Rotation forests apply PCA to random feature subsets before training each tree.

A decision list is a degenerate, one-sided tree with at most one internal node per branch; it is sparser and easier to read, but less expressive. Fuzzy decision trees allow an input to be assigned to multiple leaves with different confidence values, using fuzzy-set membership instead of hard thresholds. A decision graph generalises a tree by allowing OR as well as AND along paths, so different subtrees can share leaves, often producing models with fewer leaves than a tree of equivalent accuracy.

## Practical properties

Decision trees handle both numerical and categorical features without normalisation, perform built-in feature selection since split features matter and the rest are ignored, and can approximate any Boolean function including XOR. They are non-parametric, so they make no distributional assumption about the residuals. The flip side is instability, greediness with no global optimality guarantee, and vulnerability to overfitting when grown without pruning. NP-completeness of the optimal-tree problem, established by Hyafil and Rivest in 1976, is the formal reason every practical learner relies on heuristics.

Free and open-source implementations of these algorithms are available in scikit-learn, Weka, KNIME, Orange, R packages such as rpart and party, and ALGLIB, with commercial equivalents in MATLAB, SAS Enterprise Miner, and IBM SPSS Modeler.

Source: adapted from "Decision tree learning" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Decision_tree_learning

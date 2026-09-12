# Neural architecture search

Neural architecture search (NAS) automates the design of artificial neural networks (ANNs), the layered models used in machine learning. NAS has produced networks that match or outperform hand-designed ones. The process rests on three choices: a **search space**, which defines what kinds of networks are allowed; a **search strategy**, the method that explores that space; and a **performance estimation strategy**, which scores candidate architectures from their description without fully training them. NAS is a subfield of AutoML (automated machine learning) and overlaps with hyperparameter optimisation and meta-learning.

## Reinforcement learning

Barret Zoph and Quoc Viet Le used reinforcement learning (RL) to grow architectures one layer at a time, with the controller's reward driven by validation accuracy on a small proxy dataset. On CIFAR-10 this produced an architecture with a 3.65% error rate, 0.09% better and 1.05x faster than the best hand-designed rival. On Penn Treebank the same approach built a recurrent cell that beat LSTM with a test perplexity of 62.4 (3.6 better than the prior leader) and reached 1.214 bits per character.

Training on a large dataset directly is expensive. NASNet searched on a small dataset, then transferred a learned **cell**, a small repeating block, to a larger one. The cell has two forms: a normal cell that preserves feature-map height and width, and a reduction cell that halves them (its first operation uses a stride of two, meaning it skips every other position). Cells discovered on CIFAR-10 and stacked for ImageNet hit 82.7% top-1 and 96.2% top-5 accuracy while using 28% fewer FLOPs (floating-point operations) than the best human design. The same cells, dropped into Faster-RCNN, lifted COCO object-detection performance by 4.0%.

Efficient Neural Architecture Search (ENAS) kept RL but had a controller pick a subgraph inside one large computational graph, with all child models sharing parameters. On CIFAR-10 it reached 2.89% test error, and on Penn Treebank a test perplexity of 55.8, using 1000-fold less compute than standard NAS.

## Evolutionary algorithms

Evolutionary NAS starts with a pool of architectures scored by validation fitness. Each round, top candidates are mutated: swapping a 3x3 convolution for a 5x5, adding or removing a layer, changing a layer type, or altering hyperparameters. The worst performers are then replaced. On CIFAR-10 and ImageNet, evolution and RL perform comparably, and both slightly beat random search.

## Bayesian optimisation and hill climbing

Bayesian optimisation (BO) models the mapping from architecture to validation error with a surrogate (an approximate model of the true function), then picks the next architecture by maximising an acquisition function such as expected improvement, which balances exploring new regions and exploiting known good ones. Each evaluation still requires training, so BO is heavy. BANANAS paired BO with a neural predictor and reported promising results. A separate hill-climbing method applies network morphisms (small edits that preserve the network's function) followed by short cosine-annealing (a learning-rate schedule that smoothly cycles down) training runs; on CIFAR-10 it produced a sub-5%-error network in about 12 hours on a single GPU.

## Multi-objective search

Most NAS targets accuracy alone, yet deployment also cares about memory, model size and inference time. Multi-objective search optimises several at once. LEMONADE is an evolutionary algorithm that uses Lamarckian inheritance, where offspring inherit their parent's trained weights, to extend the Pareto frontier (the set of architectures where no other is better on all objectives) of the population. Neural Architect is an RL-based method that encodes a current network into a trainable embedding, then has a controller propose transformations; separate performance-prediction networks estimate accuracy and training time, and a reward engine combines them.

## One-shot and differentiable NAS

RL and evolution-based methods burn thousands of GPU-days. Modern approaches instead define one **supernet**, a directed acyclic graph whose edges are shared across many candidate sub-architectures, and learn the weights and the architecture parameters at once. Methods like DARTS relax the discrete choice of operation into a continuous softmax over options (a weighted average approximating the best one), letting gradients flow through the choice itself. This differentiable NAS shrinks search to a few GPU-days. DARTS, however, tends to collapse onto skip connections (identity shortcuts that bypass layers) and generalises poorly; later methods added Hessian-norm regularisation (a penalty on the curvature of the validation loss) and adversarial smoothing to stabilise the search.

Supernet-based search has closed the accuracy gap too. FBNet beat the speed-accuracy curve of mNASNet and MobileNetV2 on ImageNet using over 400x less search time than mNASNet. SqueezeNAS did the same against MobileNetV3 on the Cityscapes segmentation dataset while using over 100x less search time than its RL-based counterpart.

## Benchmarks

NAS's appetite for compute drives a large carbon footprint. NAS benchmarks fix a dataset split, a search space and a training pipeline, so a researcher can query a predicted (surrogate benchmark) or pre-recorded (tabular benchmark) final accuracy in seconds on a CPU. A surrogate benchmark predicts performance from the architecture description using a trained model; a tabular benchmark returns actual scores for architectures already trained to convergence.

| Family | Idea | Compute cost |
|---|---|---|
| RL / evolution | Generate, train, score many candidates | ~1000s of GPU-days |
| Bayesian optimisation | Surrogate + acquisition function | Heavy per evaluation |
| Differentiable / one-shot | One supernet, gradient over architecture | A few GPU-days |
| Benchmark query | Look up or predict | Seconds on a CPU |
```

Source: adapted from "Neural architecture search" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Neural_architecture_search

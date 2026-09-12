# Knowledge graph embedding

A knowledge graph stores facts as triples *(head, relation, tail)*, such as (Paris, capital_of, France). Real graphs contain thousands of entities and relations, and many plausible facts are missing. Knowledge graph embedding (KGE) translates every entity and every relation into a low-dimensional vector so that the geometry of the vectors captures which triples are true. Once the graph is embedded, a model can score any candidate triple, rank possible missing entities, and generalise to facts it has never seen.

## Defining a KGE

A KGE is specified by four choices:

- **Representation space**, the vector space (typically real or complex) in which entities and relations live, with embedding dimension *d*. Entities and relations may use different dimensions.
- **Scoring function** *f_r(h,t)* that rates a triple as plausible or not.
- **Encoding model**, the way head and relation interact to predict the tail.
- **Additional information**, such as text descriptions, types, or weights, folded into the score via an ad hoc term.

Each model family makes a different bet about what geometric operation turns a head into a tail.

## Training procedure

Every KGE algorithm follows the same recipe. Entity and relation vectors start at random values. Training runs in iterations: a batch of *b* real triples is sampled, each real triple is paired with a corrupted triple in which the head or tail has been swapped for a random wrong entity, and the embeddings are updated to push the score of true triples up and corrupted ones down. Training stops when the model begins to overfit the training set.

## Evaluation metrics

Three metrics dominate:

- **Hits@K**: fraction of test triples whose correct answer appears in the model's top *K* ranked predictions, usually *K*=10. Larger is better; values lie in [0,1].
- **Mean rank (MR)**: average position of the correct answer across all test triples. Smaller is better.
- **Mean reciprocal rank (MRR)**: average of 1/rank across the test set, which rewards near-perfect rankings. Larger is better; values lie in [0,1].

## Applications

KGE powers several downstream tasks. **Knowledge graph completion** fills in missing entities or relations; its sub-tasks are entity (link) prediction and relation prediction. **Triple classification** decides whether a triple is true by thresholding the score. **Clustering** groups similar entities from their vectors. In production, recommender systems use KGE to inject item-correlation structure without the data hunger of reinforcement learning or collaborative filtering; drug repurposing applies link prediction over biomedical knowledge graphs to propose new drug–disease links; social-political analysis mines relational patterns from embedded graphs.

## Model families

Models cluster into three families.

**Tensor decomposition models** treat the graph as a third-order tensor recording relation presence between entities and factorise it into low-dimensional vectors. Bilinear variants include DistMult, whose diagonal relation matrix is fast but blind to asymmetric facts, and ComplEx, which moves to complex vectors and the Hermitian product to recover asymmetry. ANALOGY adds an inductive-reasoning objective that subsumes DistMult, ComplEx, and HolE. SimplE learns separate head and tail vectors for each entity and averages them with an inverse relation, handling asymmetry at the cost of more parameters. TuckER applies Tucker decomposition with a shared core tensor whose weights are learned alongside the embeddings, and is fully expressive in the sense that RESCAL, DistMult, ComplEx, and SimplE are special formulations of it.

**Geometric models** treat relations as transformations applied to the head, scoring the distance to the tail: *f_r(h,t) = δ(τ(h,r), t)*. Pure translational models, inspired by word2vec, require *h + r ≈ t*. TransE is the simplest instance but struggles with one-to-many, many-to-one, and asymmetric relations. TransH projects entities onto a relation-specific hyperplane, TransR uses separate entity and relation spaces, and TransD replaces the expensive projection matrix with two vectors per entity–relation pair, one for meaning and one for the dynamic mapping. Roto-translational models substitute rotation for translation: RotatE represents each relation as a rotation in complex space (Hadamard product with unit modulus) and captures symmetric, asymmetric, inversion, and composition relations.

**Deep learning models** use neural networks to capture patterns that distance-based models miss. Convolutional variants are popular because they pack expressive power into few parameters. ConvE reshapes and concatenates the head and relation embeddings, applies a 2D convolution and a dense layer, then takes an inner product with every candidate tail in a fast 1-N evaluation, using roughly 8× fewer parameters than DistMult at similar quality. ConvKB feeds the unreshaped concatenation *[h; r; t]* through 1×3 filters into a single-neuron dense layer, framing triple scoring as binary classification. Capsule networks such as CapsE keep spatial information by routing convolutional features into capsules whose output length signals triple truth. Recurrent models like RSN learn relational paths from random walks, capturing multi-step dependencies that single-fact models ignore.

## Benchmarks

Link prediction is the standard evaluation, tested on FB15k, WN18, FB15k-237, WN18RR, and YAGO3-10. On FB15k, ComplEx reaches Hits@10 of 0.905 with MR of 34; on the sparser FB15k-237 and WN18RR, the best Hits@10 scores fall to roughly 0.52–0.58, reflecting the difficulty of leakage-resistant splits. These benchmarks have been criticised as far from real-world deployment, motivating newer splits. Open-source libraries such as PyKEEN, AmpliGraph, DGL-KE, Pykg2vec, and OpenKE implement most of these models.

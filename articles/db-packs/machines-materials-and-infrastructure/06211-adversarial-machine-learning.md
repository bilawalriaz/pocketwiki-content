# Adversarial machine learning

Adversarial machine learning studies attacks on machine learning systems and the defenses against them. Most learners are trained and tested on data assumed to come from the same statistical distribution (IID: independent and identically distributed). When an adversary can manipulate the data that reaches a model, that assumption breaks, and the model can be steered into wrong predictions, leaked training data, or corrupted behavior.

## Why models are vulnerable

Modern classifiers, especially deep neural networks, are trained to minimize loss over a finite set of examples. The optimization only guarantees smooth behavior near the training distribution, not everywhere in input space. An attacker searches for points just outside that region where the model is confident but wrong. In 2014, Christian Szegedy and colleagues showed that small, carefully crafted pixel changes, imperceptible to humans, cause state-of-the-art image classifiers to misclassify with high confidence. The same effect has since been demonstrated in speech recognition, text classification, malware detection, and reinforcement learning.

An *adversarial example* is a perturbed input that looks normal to a human but causes a model to output a wrong prediction. Perturbations are usually constrained by a small distance bound, often the L2 or L∞ norm (standard measures of pixel difference), to keep the change imperceptible.

## Main attack categories

**Evasion attacks** modify inputs at test time so a trained model misclassifies them. Spammers insert "good words" into junk mail; malware authors pad binaries to slip past antivirus; stickers on a stop sign can make a self-driving car read it as a speed limit sign. Evasion does not require touching the training data.

**Data poisoning** injects crafted examples into the training set so the learned model behaves badly. It is the leading concern in industrial deployments, in part because user-generated content (reviews, posts, uploaded images) flows straight into training pipelines. A *backdoor attack* is a poisoning variant: the model behaves normally until it sees a hidden trigger, such as a tiny patch on an image, then produces the attacker's chosen output.

**Byzantine attacks** target distributed training. When many devices, such as phones in federated learning, contribute gradients to a shared model, a minority of malicious participants can push the model off course. Defenses rely on robust gradient aggregation rules that filter or down-weight suspicious updates, though provable guarantees break down when honest participants have very different data.

**Model extraction and membership inference** attack confidentiality rather than integrity. By querying a model, an adversary can reconstruct a similar model (extraction) or determine whether a specific record was in the training set (membership inference), a problem for any model trained on medical, financial, or personal data.

## How adversarial examples are built

Two main settings govern the attacker's power. In *white-box* attacks, the adversary knows the model's architecture and weights, so gradients can be computed directly. The Fast Gradient Sign Method (FGSM), introduced by Goodfellow, Shlens, and Szegedy in 2015, takes a single step in the direction that increases loss: perturbed input = original + epsilon × sign(gradient of loss). The Carlini and Wagner (C&W) attack formulates the problem as a constrained optimization that minimizes perturbation size while forcing a target misclassification, producing harder-to-detect examples that also bypass defensive distillation.

In *black-box* attacks, the adversary only sees inputs and outputs, so gradients must be estimated by many queries. Score-based methods such as Square Attack (2020) randomly perturb small square regions and keep the change if the loss improves. Decision-based methods such as HopSkipJump need only the predicted class, and approximate the gradient by sampling around the decision boundary.

## Defenses and their limits

The standard defense is *adversarial training*: augment the training set with adversarial examples so the model learns to classify them correctly. This works but typically costs accuracy on clean data, a robustness–accuracy trade-off first analyzed in linear models and shown in deep networks by Tsipras and colleagues in 2019. Other proposed defenses include defensive distillation, ensembles, and gradient masking. Athalye and colleagues showed in 2018 that obfuscated gradients give a false sense of security and can be circumvented. No defense is proven robust against all attackers, and each is usually evaluated against a specific threat model.

## Why this is harder in real security settings

Applying machine learning to malware detection, intrusion detection, or biometric authentication runs into problems that standard benchmarks hide. *Concept drift* means malicious samples change as attackers adapt. *Class imbalance* is severe: malicious traffic may be 0.01% to 2% of total data, so a model that always predicts "benign" can be 98% accurate and useless. A study applying BERT to Android activity sequences reported an F1 score of 0.919 on a dataset where only 0.5% of samples were malicious, a substantial gain over LSTM and n-gram baselines. Other recurring pitfalls include time-based leakage between train and test sets when related malware samples appear on both sides, unstable antivirus labels that differ across engines, and data snooping, where test-set information leaks into model tuning.

## Where the field stands

Industry has responded with open-source robustness toolkits from Google, Microsoft, and IBM. Researchers such as Nicholas Frosst at Google Brain have pointed out that adversarial examples are easier to produce in laboratory conditions than in the physical world, where small rotations, lighting changes, and real physics can destroy a perturbation. Frosst also argues that the field incorrectly assumes a model trained on one data distribution will still perform well on a very different one, a gap current defenses do not close.

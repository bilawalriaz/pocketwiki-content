# Contrastive Language–Image Pre-training

Contrastive Language–Image Pre-training (CLIP) is a technique released by OpenAI on 5 January 2021 and written in Python under an MIT licence. It trains a pair of neural networks so that images and their captions end up as vectors in a single shared space: matching text and image sit close together, mismatches sit far apart. The resulting encoders power cross-modal retrieval, text-to-image generation, and aesthetic ranking.

## The core idea

Training needs only one supervision signal: a dataset of image–caption pairs. A text encoder reads the caption and outputs a vector; an image encoder reads the picture and outputs a vector of the same length. Training pulls paired vectors together and pushes unpaired vectors apart using a contrastive objective, where similarity is measured by dot product. No class labels are required, which is what enables zero-shot use later.

## How the loss works

Training proceeds in batches of *N* image–caption pairs. For each image, the model computes dot products with all *N* captions, turns them into a probability distribution with softmax, and compares to the one-hot target identifying the correct caption. The same calculation runs in reverse (image-from-text), and the two cross-entropies are averaged, giving the symmetric multi-class N-pair loss:

$$-\frac{1}{N}\sum_i \ln\frac{e^{v_i \cdot w_i / T}}{\sum_j e^{v_i \cdot w_j / T}} - \frac{1}{N}\sum_j \ln\frac{e^{v_j \cdot w_j / T}}{\sum_i e^{v_i \cdot w_j / T}}$$

Temperature *T > 0* sharpens or softens the distribution; in the original CLIP it is parameterised as *T = e^(−τ)* with τ learned during training. SigLIP replaces the softmax cross-entropy with a sigmoid loss applied independently to every pair, scaling better to very large batches.

## The two encoders

The image encoder is usually a Vision Transformer (ViT), named by size and patch (ViT-B/32, ViT-L/14, with sizes B, L, H, G and patch size in pixels). The original OpenAI release also offered ResNets; OpenCLIP by LAION uses ConvNeXt. Inputs are preprocessed by normalising each colour channel with the WIT dataset's mean and standard deviation, scaling the short side to the native resolution, and centre-cropping.

The text encoder in the original CLIP is a 12-layer, 512-wide Transformer with 8 attention heads and about 63 million parameters, using lower-cased byte-pair encoding with a 49,152-token vocabulary and a context length of 77 tokens. Captions are bracketed by [SOS] and [EOS] tokens; the final text vector is the highest-layer activation at [EOS], followed by LayerNorm and a linear projection to the shared embedding dimension (512 to 1024 depending on the image encoder).

## Training data and cost

OpenAI's models were trained on WebImageText (WIT), roughly 400 million image–caption pairs scraped from the web, with a total text volume comparable to GPT-2's WebText (~40 GB). WIT's text queries were seeded from words appearing at least 100 times in English Wikipedia, extended with high-mutual-information bigrams, names of frequently searched Wikipedia articles, and WordNet synsets. The dataset is private. ALIGN (Google) used more than one billion alt-tag pairs, and OpenCLIP used the public LAION-400M, LAION-2B, and DataComp-1B.

In the original report, 5 ResNets and 3 ViTs were each trained for 32 epochs; the largest ResNet took 18 days on 592 V100 GPUs and the largest ViT 12 days on 256 V100 GPUs. The best model, ViT-L/14, was later boosted to 336×336 resolution using FixRes. OpenCLIP's ViT-L/14 was trained for 160 epochs (~32 billion samples) on 384 A100 GPUs.

## What it enables

Because the two encoders share a vector space, CLIP performs zero-shot image classification by comparing an image to prompts like "A photo of a {class}." and picking the class with the highest dot product, with no task-specific training. The same alignment powers cross-modal retrieval, finding images from text or text from images without explicit annotations, and underpins systems like Stable Diffusion, which feeds CLIP's text embeddings into a diffusion model. Frozen CLIP encoders also act as drop-in feature extractors: DeepMind's Flamingo combined a frozen CLIP image encoder with a frozen Chinchilla language model, training only a thin connector between them, and fine-tuned CLIP variants rank images by aesthetic quality and generate image captions.

Source: adapted from "Contrastive Language–Image Pre-training" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Contrastive_Language%E2%80%93Image_Pre-training

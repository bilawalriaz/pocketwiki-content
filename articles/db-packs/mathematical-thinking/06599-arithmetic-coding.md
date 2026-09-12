# Arithmetic coding

Arithmetic coding is a lossless compression method that represents an entire message as a single fractional number between 0 and 1. The interval [0, 1) is divided into sub-intervals whose sizes match the probabilities of the symbols. Encoding reads the message one symbol at a time, narrowing the interval to whichever sub-interval matches the current symbol. Any number inside the final narrow interval uniquely identifies the message. Because probable symbols get larger sub-intervals, they require fewer bits to pinpoint, and the output length approaches the source entropy, the minimum average bits per symbol established by Shannon's source coding theorem.

## A simple example

Suppose a model assigns four symbols the following cumulative ranges in [0, 1): NEUTRAL 0.0–0.6 (probability 0.6), POSITIVE 0.6–0.8 (0.2), NEGATIVE 0.8–0.9 (0.1), END-OF-DATA 0.9–1.0 (0.1). Encoding NEUTRAL, NEGATIVE, END-OF-DATA: after NEUTRAL the interval is [0, 0.6); after NEGATIVE it narrows to [0.48, 0.54); after END-OF-DATA the final interval is [0.534, 0.540). Any number inside it, such as 0.538, identifies the message.

To decode, the receiver applies the same model to the same starting interval, finds which sub-interval contains 0.538 (NEUTRAL), then partitions that sub-interval and checks again, repeating until the END-OF-DATA marker appears. The encoder and decoder must share the same model; otherwise the partitions disagree and the message is lost. Only enough digits of the fraction are transmitted to place the decoder inside the final interval, so the output forms a prefix code: no valid code for one message is also a prefix of another.

## Why probabilities matter

Compression requires unequal probabilities. When every symbol is equally likely, all sub-intervals are the same size and the entropy reaches log₂(n) bits per symbol for an alphabet of size n, leaving nothing to remove. Fair coin flips sit at exactly 1 bit per symbol and cannot be compressed. Skewed distributions help: a binary source with probabilities 0.9 and 0.1 has entropy near 0.469 bits per symbol, so arithmetic coding reaches a ratio of roughly 2.1:1.

## Models, adaptation, and precision

The probability model is the encoder's prediction of which symbols will appear; better predictions yield tighter intervals and shorter output. Static models use fixed probabilities. Higher-order models condition each probability on preceding symbols, so "u" becomes much more likely after "q". Adaptive models update probabilities as the message is processed, provided the decoder applies identical updates at each step.

A practical encoder cannot store infinite precision, so it works at a fixed bit width and uses renormalization: whenever the interval's endpoints begin sharing their leading bits, those bits are emitted, the interval shifts left, and fresh low-order bits are introduced. This keeps precision fixed while letting the encoded message grow without bound.

For the example above, the entropy of NEUTRAL, NEGATIVE, END-OF-DATA is −log₂(0.6) − log₂(0.1) − log₂(0.1) ≈ 7.381 bits, but binary output must be an integer number of bits, so the encoder uses at least 8 bits, a slack of less than 1 bit that shrinks as messages grow. A wrong model can also make the output larger than the input.

## Equal probabilities and radix conversion

When all symbols are equally likely, arithmetic coding reduces to a change of base. A six-symbol message over three equally likely symbols is equivalent to a six-digit base-3 number, which can be converted to binary in place and back again for decoding, saving about two bits per six symbols compared with naive two-bit-per-symbol block coding.

## Comparison with Huffman coding

Huffman coding assigns each symbol a whole-bit code, so it reaches entropy only when every symbol probability is a power of two. For a binary source with probabilities 0.95 and 0.05, naive Huffman coding transmits 1 bit per symbol, while arithmetic coding reaches the entropy limit of about 71.4% compression. Grouping Huffman symbols into blocks of three closes the gap somewhat, reaching about 56.7% compression, but requires exponentially larger code tables and is rarely as practical as arithmetic coding.

## Origin and patents

The basic algorithms were developed independently in 1976 by Jorma J. Rissanen at IBM Research and by Richard C. Pasco at Stanford, both publishing in May of that year. Numerous subsequent refinements were patented, mostly by IBM, which restricted adoption in standards like JPEG; most of those patents have since expired, and modern formats including JPEG XL, PackJPG, Brunsli, and Lepton can recover about 25% size savings by re-encoding JPEG files with arithmetic coding or asymmetric numeral systems. The Dirac video codec uses arithmetic coding and has not been patented.

Source: adapted from "Arithmetic coding" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Arithmetic_coding

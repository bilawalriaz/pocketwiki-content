# Digital Signature Algorithm

The Digital Signature Algorithm (DSA) is a public-key signature standard based on modular exponentiation (computing `a^b mod n` for large `a`, `b`, `n`) and the discrete logarithm problem: given `g`, `p`, and `y = g^x mod p`, recovering `x` is computationally intractable. A signer holds a private key `x` and publishes the matching public key `y = g^x mod p`. The private key produces a short signature that anyone holding `y` can verify, and forging signatures without `x` requires solving the discrete logarithm. DSA is a variant of the Schnorr and ElGamal schemes and was adopted by the U.S. National Institute of Standards and Technology as FIPS 186 in 1994, with a final 2023 revision (FIPS 186-5) that forbids generating new DSA signatures while still permitting verification of old ones.

A valid DSA signature provides three properties: **authentication** (the verifier confirms the signer's identity), **integrity** (the message cannot be altered after signing without invalidating the signature), and **non-repudiation** (the signer cannot later deny producing the signature).

## Parameters and key generation

All DSA users share domain parameters `(p, q, g)` chosen once and reused.

1. Pick an approved hash function `H` (originally SHA-1; SHA-2 is now preferred).
2. Pick a prime `p` of `L` bits and a prime `q` of `N` bits, with `N < L`, `N ≤ |H|`, and `q` dividing `p − 1`. FIPS 186-4 fixes `(L, N)` to one of (1024, 160), (2048, 224), (2048, 256), or (3072, 256).
3. Choose an integer `h` from `{2, …, p−2}` and compute `g = h^((p−1)/q) mod p`, retrying if `g = 1`. Usually `h = 2`. By Fermat's little theorem, `g^q ≡ 1 (mod p)`, so `g` has order `q`: every power of `g` reduces mod `q` to one of `q` distinct values.

Each user picks a private key `x` at random from `{1, …, q−1}` and computes the public key `y = g^x mod p`. The user publishes `y` over a reliable but not necessarily secret channel and keeps `x` secret.

## Signing

To sign a message `m`, the signer:

1. Picks a fresh random `k` from `{1, …, q−1}`.
2. Computes `r = (g^k mod p) mod q` (retry with a new `k` if `r = 0`).
3. Computes `s = (k^(−1) · (H(m) + x·r)) mod q` (retry if `s = 0`). Here `k^(−1)` is the modular inverse of `k` modulo `q`, the value such that `k · k^(−1) ≡ 1 (mod q)`.

The signature is the pair `(r, s)`. The expensive `g^k` step can be precomputed before the message is known.

## Verification

To check a signature `(r, s)` on `m`, the verifier:

1. Confirms `0 < r < q` and `0 < s < q`.
2. Computes `w = s^(−1) mod q`, then `u₁ = H(m)·w mod q` and `u₂ = r·w mod q`.
3. Computes `v = (g^u₁ · y^u₂ mod p) mod q`.

The signature is valid if and only if `v = r`. The check works because `g` has order `q`: substituting `s^(−1)(H(m) + xr)` for `k` gives `g^k ≡ g^(H(m)w) · g^(xrw) ≡ g^u₁ · y^u₂ (mod p)`, and the outer `mod q` reproduces the same `r` the signer produced.

## The critical role of the random `k`

DSA's security collapses if the per-message value `k` is reused, predictable, or leaks even a few bits across signatures: any of these can be inverted to recover the private key `x`. The same flaw exists in ECDSA, and in December 2010 the group fail0verflow extracted Sony's ECDSA key for the PlayStation 3 because Sony reused `k` across signatures. The standard fix, RFC 6979, derives `k` deterministically from the private key and the message hash, guaranteeing uniqueness without a trusted random source. The same machinery can also be turned against the user: a malicious implementation can craft `k` values that subliminally leak the private key through signatures that all verify correctly.

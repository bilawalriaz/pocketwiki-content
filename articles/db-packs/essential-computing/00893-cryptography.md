# Cryptography

Cryptography is the practice of designing protocols that let two parties communicate so adversaries cannot read their messages; the companion field, cryptanalysis, studies how to break those protocols. The field underlies electronic commerce, payment cards, digital currencies, password storage, and military communications.

## Core terminology

Encryption turns readable *plaintext* into unreadable *ciphertext*; decryption reverses the process, and both are governed by a secret string called a *key*. A *cipher* is the pair of encryption and decryption algorithms together with the key. Conventional examples name the sender "Alice," the recipient "Bob," and the eavesdropper "Eve."

Two kinds of cryptosystem exist. In *symmetric* cryptography the same key encrypts and decrypts; symmetric ciphers are fast and were the only kind known before the 1970s. In *asymmetric*, or *public-key*, cryptography each user holds a paired public key (freely shared) and private key (kept secret). Because public-key operations are slow, practical systems use asymmetric crypto only to exchange a fresh symmetric key, then switch to symmetric encryption for the conversation. A *code* replaces whole words or phrases; a cipher operates below that level, on letters or bits. *Steganography* hides the existence of a message rather than its content, using tools such as invisible ink or microdots.

## Classical foundations

Classical ciphers fall into two families. *Transposition* ciphers rearrange the letters of a message. *Substitution* ciphers replace each letter with another; the Caesar cipher, which shifts every letter three places, is the familiar example. Because any fixed substitution preserves the statistical patterns of the underlying language, *frequency analysis*, attributed to the ninth-century Arab scholar Al-Kindi, broke nearly every classical cipher.

The breakthrough came with the *polyalphabetic* cipher, developed by Leon Battista Alberti around 1467, which uses several different substitution alphabets within a single message. The Vigenère cipher, based on a keyword, was long thought secure until Charles Babbage showed how to crack it in the mid-nineteenth century; Friedrich Kasiski published the same method, now called Kasiski examination, about ten years later. In 1883 Auguste Kerckhoffs distilled the lesson into a principle still quoted today: the security of a system must rest on keeping the key secret, not on keeping the algorithm secret. Claude Shannon later restated it as "the enemy knows the system."

## The modern era

The Second World War accelerated the field. British cryptanalysts at Bletchley Park built Colossus, the first fully electronic, digital, programmable computer, to read German Lorenz traffic. Open academic research then expanded rapidly. In the early 1970s IBM designed DES, the first US federal encryption standard. In 1976 Whitfield Diffie and Martin Hellman published public-key key exchange, and in 1977–1978 Ronald Rivest, Adi Shamir, and Leonard Adleman published RSA, the most widely used public-key algorithm. A 1997 GCHQ document revealed that James Ellis, Clifford Cocks, and Malcolm Williamson had developed the same ideas in classified work between roughly 1970 and 1974.

Modern security rests on *computational hardness assumptions* such as the difficulty of factoring large integers or computing discrete logarithms; such systems are called "computationally secure" because no proof rules out a faster attack, only its absence today. The one-time pad, in which the key is truly random, at least as long as the message, never reused, and kept secret, is the only cipher Shannon proved unbreakable, a property called *information-theoretic security*. Because such keys are impractical to distribute, almost all real systems rely on computational security instead.

## Symmetric ciphers

Symmetric ciphers come in two forms. A *block cipher* encrypts fixed-size blocks of plaintext; examples include DES (now withdrawn) and its successor AES, which dominates x86 hardware thanks to AES-NI instructions. A *stream cipher* generates a keystream that is combined bit by bit with the plaintext, behaving like a mechanical one-time pad; RC4 was long a popular example. To verify that a message has not been tampered with, senders append a *message authentication code*, a keyed hash, or in public-key settings a *digital signature*, which is easy to produce with the private key but hard to forge without it and is bound to the message content.

*Hash functions* compress any input to a fixed-length fingerprint and are designed to resist *collisions* (two inputs producing the same fingerprint) and *preimage* attacks (recovering the input from the output). MD4 and MD5 are broken, SHA-1 has known attacks, and SHA-3 (Keccak, selected by NIST on 2 October 2012) is the current contest winner.

## Public-key cryptography

The reason public-key cryptography matters is that symmetric key management scales poorly: in a network of *n* members each user must securely hold *n − 1* distinct keys. Diffie and Hellman's 1976 paper proposed a way for two parties to establish a shared secret over an open channel, and Rivest, Shamir, and Adleman delivered the first practical public-key encryption and signature scheme shortly after. Digital signatures anchor public-key infrastructures, SSL, and TLS.

Because public-key operations are expensive, real systems are *hybrid*: RSA or elliptic-curve key exchange negotiates a fresh symmetric session key, and AES or ChaCha20 encrypts the bulk traffic. *Elliptic-curve cryptography* offers equivalent security to RSA with much smaller keys, which is why it dominates mobile and embedded devices. The looming threat is quantum computing, which could reduce the time to break RSA and elliptic-curve systems from millennia to seconds, motivating *post-quantum cryptography* based on lattice, code, hash, and multivariate-quadratic problems.

## Cryptanalysis and limits

Attackers sort their tools by what they can observe. A *ciphertext-only* attack sees only scrambled messages; a *known-plaintext* attack has some plaintext-ciphertext pairs; a *chosen-plaintext* attack can ask the oracle to encrypt chosen messages; a *chosen-ciphertext* attack can ask it to decrypt; and a *man-in-the-middle* attack intercepts and rewrites traffic between two parties. Implementation mistakes often matter more than mathematics: timing differences, power consumption, and careless key handling have toppled more real systems than clever algebra. Coercion and social engineering remain the cheapest tools an adversary has.

## Legal and political context

Governments have long treated strong encryption as a weapon. France restricted domestic use until 1999; China and Iran require licenses; several other countries remain restrictive. In Bernstein v. United States (1999), a US court held that cryptographic source code is protected speech. The 1998 Digital Millennium Copyright Act criminalised circumvention of digital locks, chilling some research; the 1996 Wassenaar Arrangement once capped exported key lengths, a limit largely lifted in 2000. The United Kingdom, Australia, and France can compel suspects to hand over decryption keys; whether the Fifth Amendment shields passphrases in the United States remains contested after *United States v. Fricosu* (2012) and the 2016 FBI–Apple dispute.

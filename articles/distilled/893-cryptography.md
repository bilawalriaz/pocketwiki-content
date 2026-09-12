# Cryptography

## Overview
Cryptography is the practice and study of techniques for secure communication in the presence of adversaries. Historically synonymous with encryption (converting plaintext to ciphertext), modern cryptography intersects mathematics, computer science, and engineering to provide data confidentiality, integrity, authentication, and non-repudiation. It underpins critical infrastructure including electronic commerce, digital currencies, and military communications. The field shifted from linguistic patterns to mathematical theory in the 20th century, establishing computationally secure systems based on hard mathematical problems (e.g., integer factorization) and information-theoretically secure schemes like the one-time pad. Legal tensions persist regarding export controls, government access to keys, and digital rights management.

## Timeline
- **c. 1900 BCE** — Earliest known ciphertext carved on stone in Egypt.
- **c. 50 BCE** — Julius Caesar uses substitution cipher (shift of three) for military communications.
- **9th century** — Al-Kindi writes *Risalah fi Istikhraj al-Mu'amma*, describing frequency analysis cryptanalysis.
- **1467** — Leon Battista Alberti develops the polyalphabetic cipher and cipher disk.
- **1883** — Auguste Kerckhoffs publishes Kerckhoffs's Principle: security should rely only on key secrecy.
- **1917–1918** — Rotor cipher machines developed during World War I.
- **1939–1945** — Bletchley Park cryptanalysis (Enigma, Lorenz) spurs development of Colossus, the first programmable digital computer.
- **1948–1949** — Claude Shannon publishes papers founding information theory and mathematical cryptography.
- **1976** — Diffie and Hellman publish Diffie–Hellman key exchange, introducing public-key cryptography.
- **1977** — RSA algorithm published by Rivest, Shamir, and Adleman.
- **1977** — Data Encryption Standard (DES) adopted as US federal standard.
- **1991** — PGP source code released on the Internet, triggering US export investigation.
- **1999** — Bernstein v. United States rules cryptographic source code is protected free speech.
- **2000** — US significantly relaxes cryptography export controls.
- **2001** — Advanced Encryption Standard (AES) replaces DES.
- **2012** — NIST selects Keccak as SHA-3 hash standard.
- **2017** — Nature review surveys post-quantum cryptography families (lattice, code, multivariate, hash-based).

## Body

### Classic Cryptography
Before the modern era, cryptography focused solely on message confidentiality via encryption. Classical ciphers comprised **transposition ciphers** (rearranging letter order) and **substitution ciphers** (replacing letters/groups). Early examples include the Caesar cipher (shift substitution), Atbash (Hebrew), and the Spartan scytale (transposition). **Steganography** (hiding a message's existence) appeared anciently, e.g., tattooing a slave's head. In the 9th century, Arab scholars systematized cryptanalysis: Al-Khalil used permutations/combinations, and Al-Kindi invented **frequency analysis**, which breaks monoalphabetic ciphers by exploiting language letter statistics. This rendered simple ciphers vulnerable, though many attackers remained unaware of the technique. The **polyalphabetic cipher** (Alberti, c. 1467; Vigenère variant) countered frequency analysis by using multiple substitution alphabets controlled by a key. In the 19th century, Babbage and Kasiski broke Vigenère via **Kasiski examination**. Auguste Kerckhoffs (1883) and later Claude Shannon formalized the principle that a cipher must remain secure even if the adversary knows the algorithm (**Kerckhoffs's Principle** / **Shannon's Maxim**). Mechanical aids evolved from cipher disks to rotor machines (e.g., Enigma, late 1920s), substantially increasing cryptanalytic difficulty after WWI.

### Early Computer-Era Cryptography
WWII cryptanalysis at Bletchley Park (UK) drove the creation of Colossus, the first fully electronic programmable computer, to break the German Lorenz cipher. Extensive open academic research began in the mid-1970s. IBM designed the **Data Encryption Standard (DES)**, adopted as the first US federal standard (1977). In 1976, Diffie and Hellman published the **Diffie–Hellman key exchange**, proving public-key cryptography feasible. The **RSA algorithm** (Rivest, Shamir, Adleman, 1977) provided the first practical public-key encryption system. Modern cryptography relies on **computational hardness assumptions** (e.g., integer factorization, discrete logarithm) making algorithms infeasible to break in practice ("computationally secure"). **Information-theoretically secure** schemes (e.g., one-time pad, proven by Shannon) are unbreakable even with unlimited computing power but are impractical for general use. Designers must anticipate future advances, such as quantum computing, which threatens current public-key systems (RSA, ECC), driving **post-quantum cryptography (PQC)** research.

### Symmetric-Key Cryptography
In **symmetric-key cryptography**, sender and receiver share the same secret key (the only known method until 1976). Ciphers are **block ciphers** (encrypt fixed-size blocks, e.g., DES, AES) or **stream ciphers** (generate a keystream combined bit-by-bit with plaintext, e.g., RC4). **AES** replaced DES as the US standard (2001); triple-DES remains in use. **Message Authentication Codes (MACs)** use a secret key to authenticate hash values, preventing attacks on bare digests. **Cryptographic hash functions** (third algorithm type) map variable-length input to fixed-length output for digital signatures and integrity. **MD4/MD5** are broken; **SHA-1** has identified attacks; **SHA-2** showed vulnerabilities (2011); **SHA-3 (Keccak)** was selected in 2012. Hash functions are one-way (non-invertible), unlike ciphers.

### Public-Key Cryptography
**Public-key (asymmetric) cryptography** uses a mathematically related key pair: a **public key** (freely distributed, encrypts) and a **private key** (secret, decrypts). This solves the symmetric key management problem (keys scale with square of network members). Diffie–Hellman (1976) demonstrated the concept via key exchange; RSA (1978) provided encryption/signatures. GCHQ (UK) later revealed prior classified discoveries: Ellis (principles, ~1970), Cocks (RSA-like, 1973), Williamson (Diffie–Hellman, 1974). Public-key algorithms rely on "hard" number theory problems: RSA on **integer factorization**, Diffie–Hellman/DSA on **discrete logarithm**, ECC on **elliptic curve discrete logarithm**. Due to computational expense (modular exponentiation), **hybrid cryptosystems** are standard: public-key encrypts a symmetric session key, which encrypts the bulk message. **Digital signatures** (RSA, DSA) provide authentication, non-repudiation, and integrity by signing a hash with a private key; verification uses the public key. They are central to PKI, SSL/TLS, and VPNs.

### Cryptanalysis
**Cryptanalysis** seeks weaknesses to subvert schemes. Shannon proved the **one-time pad** unbreakable *if* the key is truly random, never reused, secret, and ≥ message length. Most ciphers are vulnerable to **brute force** (trying all keys), but security relies on the "work factor" being exponentially dependent on key size. Attack models: **ciphertext-only**, **known-plaintext**, **chosen-plaintext** (e.g., WWII "gardening"), **chosen-ciphertext**, and **man-in-the-middle**. **Side-channel attacks** exploit physical implementation (timing, power consumption, traffic analysis) rather than algorithmic flaws. **Social engineering** (bribery, coercion) often surpasses pure cryptanalysis in cost-effectiveness. Public-key cryptanalysis targets the underlying math problems (factoring, discrete log); quantum computers (Shor's algorithm) threaten polynomial-time solutions, necessitating PQC.

### Cryptographic Primitives and Cryptosystems
**Cryptographic primitives** are basic algorithms with fundamental properties (e.g., pseudorandom functions, one-way functions). **Cryptosystems** (or protocols) combine primitives to guarantee high-level security properties (e.g., CPA security). The distinction is arbitrary (RSA is both). Examples: RSA, ElGamal, PGP, zero-knowledge proofs, secret sharing. **Lightweight cryptography (LWC)** targets constrained environments (IoT), optimizing for power, processing, and security (e.g., Ascon, SPECK).

### Applications
**Cybersecurity**: HTTPS (TLS), end-to-end encryption (WhatsApp, Signal, PGP), password hashing (storing hashes, not plaintext), full-disk encryption (BitLocker). **Cryptocurrencies**: Blockchains/DeFi rely on keys, hash functions, asymmetric encryption, MFA, E2EE, and Zero-Knowledge Proofs. **Quantum Cybersecurity**: Quantum computers could reduce RSA/ECC breaking time from millennia to seconds; migration to quantum-resistant algorithms is urgent.

### Legal Issues
**Prohibitions/Export Controls**: Governments historically classified crypto as a weapon (US Munitions List). 1990s challenges: PGP investigation (Zimmermann), *Bernstein v. US* (1999, code = speech). **Wassenaar Arrangement** (1996) liberalized short-key exports; US relaxed controls (2000), enabling global browser-based crypto (TLS). **NSA Involvement**: Influenced DES design (resistance to differential cryptanalysis, kept secret until 1990s rediscovery); **Clipper chip** (1993) proposed government key escrow, criticized for violating Kerckhoffs's Principle. **Digital Rights Management (DRM)**: **DMCA (1998)** criminalizes circumvention tools, chilling cryptanalytic research (e.g., Ferguson, Sklyarov cases). **Forced Disclosure**: UK RIP Act compels decryption (penalty: 2–5 years); similar laws in Australia, Finland, France, India. US courts split on Fifth Amendment protection (e.g., *US v. Fricosu*, 2012). **Plausible deniability** (hidden volumes) is a technical counter-measure.

## Terms
- ****Plaintext / Ciphertext**** — Readable input data / unintelligible encrypted output.
- ****Cipher**** — A pair of algorithms (encryption, decryption) controlled by a key.
- ****Key**** — Secret parameter (string of characters) controlling cipher operation; security relies solely on its secrecy (Kerckhoffs's Principle).
- ****Symmetric-key**** — Cryptosystem using the same secret key for encryption and decryption (e.g., AES, DES).
- ****Asymmetric / Public-key**** — Cryptosystem using a public key (encrypt) and private key (decrypt); enables secure communication without pre-shared secret (e.g., RSA, ECC).
- ****Cryptographic Hash Function**** — One-way function mapping variable-length input to fixed-length output; used for integrity, signatures (e.g., SHA-2, SHA-3).
- ****Digital Signature**** — Asymmetric primitive providing authentication, non-repudiation, and integrity by signing a hash with a private key.
- ****Cryptanalysis**** — Study of breaking cryptosystems without the key; includes brute force, frequency analysis, side-channel attacks.
- ****One-Time Pad**** — Information-theoretically secure cipher requiring a truly random, never-reused key ≥ message length; proven unbreakable by Shannon.
- ****Post-Quantum Cryptography (PQC)**** — Algorithms (lattice, code, hash, multivariate-based) believed secure against both classical and quantum computers.

## Debates and open questions
*   **Quantum Timeline**: When will large-scale quantum computers break RSA/ECC? Migration to PQC must precede this, but the timeline is uncertain.
*   **PQC Standardization**: Which lattice, code, hash, or multivariate schemes will survive cryptanalysis and become global standards (NIST process ongoing)?
*   **Government Access vs. Security**: Can "exceptional access" (key escrow, backdoors) be implemented without violating Kerckhoffs's Principle and creating systemic vulnerabilities?
*   **Legal Boundaries**: Does forced decryption violate rights against self-incrimination (US Fifth Amendment, similar protections elsewhere)?
*   **DRM vs. Research**: Does the DMCA (and global equivalents) legitimately protect copyright or unconstitutionally suppress security research and fair use?
*   **Provable Security**: Few systems are unconditionally secure; most rely on unproven hardness assumptions (P vs NP, factoring difficulty). A breakthrough in algorithms or math could collapse current infrastructure.
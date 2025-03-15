**I. Introduction to Cryptography**

*   Understanding basic cryptographic principles
    *   Confidentiality, Integrity, Authentication, Non-Repudiation (CIAAN)
    *   Symmetric vs. Asymmetric Cryptography

*   Historical Ciphers
    *   Caesar Cipher: Understanding substitution ciphers
        *   Manually encrypt and decrypt messages
    *   Vigenère Cipher: Exploring polyalphabetic substitution
        *   Understanding key concepts: keyword, repeating key, encryption table
        *   Manually encrypt and decrypt messages

**II. Symmetric-Key Cryptography**

*   Understanding Stream Ciphers
    *   Key stream generation
    *   Examples: RC4 (historical perspective)

*   Understanding Block Ciphers
    *   Electronic Codebook (ECB) mode: Vulnerabilities and limitations
        *   Demonstrate ECB encryption with an image
    *   Cipher Block Chaining (CBC) mode: Initialization vectors (IVs) and chaining
        *   Understanding IV requirements: Randomness, Uniqueness
    *   Counter (CTR) mode: Parallel encryption and keystream reuse
        *   Advantages and Disadvantages of CTR Mode

*   Advanced Encryption Standard (AES)
    *   AES rounds, key expansion, and S-boxes
    *   AES implementation in Python using `cryptography` library
        *   Installation: `pip install cryptography`
        *   Encrypt and decrypt messages using AES-CBC and AES-CTR

**III. Asymmetric-Key Cryptography**

*   Understanding Public and Private Keys
    *   Key generation and distribution
    *   Digital signatures and key exchange

*   RSA Algorithm
    *   Mathematical foundations: Prime number generation, modular arithmetic
    *   Key generation process: Selecting p, q, n, φ(n), e, d
    *   Encryption and decryption steps
    *   Implementing RSA in Python using `cryptography`
        *   Key generation: `rsa.generate_private_key()`
        *   Encryption/Decryption: `private_key.encrypt()`, `public_key.decrypt()`
        *   Padding schemes: OAEP

*   Diffie-Hellman Key Exchange
    *   Mathematical foundation: Discrete logarithm problem
    *   Key agreement protocol: Shared secret generation
    *   Man-in-the-middle attack vulnerabilities
    *   Elliptic-Curve Diffie-Hellman (ECDH)
        *   Advantages over standard Diffie-Hellman

**IV. Cryptographic Hash Functions**

*   Understanding Hash Function Properties
    *   Preimage resistance, second preimage resistance, collision resistance
    *   Applications: Data integrity, password storage

*   SHA-256
    *   Understanding hash function structure (high level)
    *   Implementing SHA-256 in Python using `hashlib`
        *   `hashlib.sha256(b"message").hexdigest()`

*   Password Hashing
    *   Salted hashes: Preventing rainbow table attacks
    *   Key derivation functions: PBKDF2, bcrypt, scrypt
        *   Understanding work factors and iteration counts
        *   Implementing password hashing in Python using `bcrypt` or `scrypt`

**V. Digital Signatures**

*   Understanding Digital Signature Principles
    *   Signing and verification process
    *   Non-repudiation and authentication

*   RSA Signatures
    *   Signing: Using private key to create a signature
    *   Verification: Using public key to verify the signature
    *   Implementing RSA signatures in Python using `cryptography`
        *   Signing: `private_key.sign()`
        *   Verification: `public_key.verify()`
        *   Padding schemes: PSS

*   Elliptic Curve Digital Signature Algorithm (ECDSA)
    *   Benefits of using elliptic curves for signatures

**VI. Public Key Infrastructure (PKI)**

*   Understanding Digital Certificates
    *   Certificate authorities (CAs) and trust models
    *   X.509 certificates: Structure and contents
        *   Subject, Issuer, Serial Number, Validity, Public Key

*   Certificate Revocation
    *   Certificate Revocation Lists (CRLs)
    *   Online Certificate Status Protocol (OCSP)

*   Implementing Certificate Validation in Python using `cryptography` and `requests`
    *   Downloading certificates from a server
    *   Verifying certificate chains

**VII. Applied Cryptography and Security Protocols**

*   HTTPS/TLS
    *   Understanding TLS handshake process
    *   Cipher suites and key exchange algorithms
    *   Man-in-the-middle attacks and defenses (certificate pinning)

*   Secure Shell (SSH)
    *   Key exchange, authentication, and encryption
    *   Port forwarding and tunneling

*   VPNs (Virtual Private Networks)
    *   IPSec and OpenVPN protocols
    *   Encryption and authentication mechanisms

**VIII. Cryptographic Attacks and Countermeasures**

*   Brute-Force Attacks
    *   Key space and computational complexity
    *   Countermeasures: Strong passwords, key stretching

*   Dictionary Attacks and Rainbow Tables
    *   Precomputed hash tables
    *   Countermeasures: Salting, key derivation functions

*   Side-Channel Attacks
    *   Timing attacks, power analysis
    *   Countermeasures: Constant-time algorithms, masking

*   Padding Oracle Attacks
    *   Exploiting padding errors in CBC mode encryption
    *   Countermeasures: Authenticated encryption

**IX. Advanced Cryptography Topics (Optional)**

*   Homomorphic Encryption
    *   Performing computations on encrypted data

*   Zero-Knowledge Proofs
    *   Proving knowledge without revealing the secret

*   Post-Quantum Cryptography
    *   Algorithms resistant to quantum computer attacks
    *   Examples: Lattice-based cryptography, code-based cryptography

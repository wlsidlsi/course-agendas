**I. Introduction to Cryptography**

*   Understanding Basic Concepts
    *   Defining Cryptography, Cryptanalysis, and Cryptology
    *   Exploring the Goals of Cryptography: Confidentiality, Integrity, Authentication, and Non-Repudiation (CIAAN)
    *   Distinguishing between Symmetric-key and Asymmetric-key Cryptography
*   Historical Ciphers
    *   Understanding Caesar Cipher
        *   Manual encryption and decryption examples
        *   Frequency analysis attack on Caesar Cipher
    *   Exploring Vigenère Cipher
        *   Manual encryption and decryption examples
        *   Kasiski examination and frequency analysis attacks
    *   Analyzing the weaknesses of historical ciphers

**II. Symmetric-Key Cryptography**

*   Block Ciphers
    *   Understanding Data Encryption Standard (DES)
        *   DES Algorithm Steps
        *   Limitations of DES: key size
    *   Exploring Advanced Encryption Standard (AES)
        *   AES Algorithm Steps (Rounds, SubBytes, ShiftRows, MixColumns, AddRoundKey)
        *   AES Key Sizes (128, 192, 256 bits)
        *   Practical AES encryption/decryption examples using `openssl`
    *   Cipher Modes of Operation
        *   Electronic Codebook (ECB) mode: disadvantages
        *   Cipher Block Chaining (CBC) mode: initialization vector (IV)
        *   Counter (CTR) mode: parallel processing
        *   Galois/Counter Mode (GCM): authenticated encryption
        *   Choosing the appropriate mode for different scenarios
*   Stream Ciphers
    *   Understanding RC4
        *   RC4 Algorithm
        *   Weaknesses of RC4
    *   Exploring Salsa20 and ChaCha20
        *   Advantages of Salsa20/ChaCha20 over RC4
        *   Usage in TLS 1.3

**III. Asymmetric-Key Cryptography**

*   Mathematical Foundations
    *   Understanding Prime Numbers and Modular Arithmetic
    *   Exploring Euler's Totient Function
    *   Understanding Fermat's Little Theorem
    *   Exploring the Euclidean Algorithm and Modular Inverse
*   RSA Algorithm
    *   Key Generation Process
        *   Choosing primes p and q
        *   Calculating n and φ(n)
        *   Selecting e and calculating d
    *   Encryption and Decryption Process
    *   RSA Implementation using `openssl`
    *   Understanding Padding Schemes (e.g., PKCS#1 v1.5, OAEP)
    *   Common Attacks on RSA (e.g., small e, common modulus attack) and countermeasures.
*   Elliptic Curve Cryptography (ECC)
    *   Understanding Elliptic Curves over Finite Fields
    *   Exploring Elliptic Curve Discrete Logarithm Problem (ECDLP)
    *   Key Exchange with Elliptic-Curve Diffie-Hellman (ECDH)
    *   Digital Signatures with Elliptic Curve Digital Signature Algorithm (ECDSA)

**IV. Hashing Algorithms**

*   Understanding Hash Functions
    *   Defining Hash Function Properties: Preimage Resistance, Second Preimage Resistance, Collision Resistance
    *   Exploring Common Hash Algorithms
        *   Message Digest 5 (MD5): Vulnerabilities and deprecation
        *   Secure Hash Algorithm 1 (SHA-1): Vulnerabilities and deprecation
        *   SHA-2 Family (SHA-224, SHA-256, SHA-384, SHA-512)
        *   SHA-3 Family (Keccak)
    *   Practical examples of hashing data using `sha256sum`, `sha512sum`
*   Message Authentication Codes (MACs)
    *   Understanding HMAC (Hash-based Message Authentication Code)
        *   HMAC construction and security properties
        *   Practical examples using `openssl dgst -hmac`
    *   Exploring Cipher-based Message Authentication Code (CMAC)
*   Password Hashing
    *   Understanding Salt and Pepper
    *   Exploring Adaptive Hashing Algorithms: bcrypt, scrypt, Argon2
        *   Importance of key derivation functions (KDFs)
        *   Configuring work factors (cost) for bcrypt, scrypt and Argon2

**V. Digital Signatures and Certificates**

*   Digital Signature Process
    *   Signing a message using a private key
    *   Verifying a signature using a public key
    *   Ensuring Integrity and Authenticity
*   Digital Certificates
    *   Understanding X.509 Certificates
    *   Exploring Certificate Authorities (CAs)
    *   Certificate Revocation Lists (CRLs) and Online Certificate Status Protocol (OCSP)
    *   Creating and managing self-signed certificates using `openssl`
    *   Trust Models: Web of Trust vs. Hierarchical Trust
*   Public Key Infrastructure (PKI)
    *   Understanding PKI Components
    *   Exploring Certificate Policies and Certification Practice Statements
    *   Secure Key Storage and Management

**VI. Key Exchange Protocols**

*   Diffie-Hellman Key Exchange
    *   Understanding the Diffie-Hellman Algorithm
    *   Man-in-the-Middle Attack on Diffie-Hellman
*   Diffie-Hellman with Digital Signatures
*   Secure Sockets Layer/Transport Layer Security (SSL/TLS)
    *   TLS Handshake Protocol
        *   Cipher suite negotiation
        *   Key exchange methods (e.g., RSA, Diffie-Hellman, Elliptic-Curve Diffie-Hellman)
        *   Authentication
    *   TLS Record Protocol
    *   Analyzing TLS traffic using Wireshark
*   Secure Shell (SSH)
    *   SSH Key Exchange
    *   SSH Authentication Methods

**VII. Cryptographic Attacks and Countermeasures**

*   Brute-Force Attacks
    *   Dictionary Attacks
    *   Rainbow Table Attacks
    *   Countermeasures: Key length, salting, key stretching
*   Side-Channel Attacks
    *   Timing Attacks
    *   Power Analysis Attacks
    *   Electromagnetic Attacks
    *   Countermeasures: Constant-time algorithms, masking
*   Implementation Attacks
    *   Buffer Overflows
    *   Integer Overflows
    *   Format String Vulnerabilities
    *   Countermeasures: Secure coding practices, input validation
*   Chosen Ciphertext Attacks (CCA)
    *   Padding Oracle Attacks
    *   Countermeasures: Authenticated Encryption

**VIII. Applications of Cryptography**

*   Secure Communication
    *   Email Encryption (PGP, S/MIME)
    *   Messaging Applications (Signal, WhatsApp)
    *   Virtual Private Networks (VPNs)
*   Data Security
    *   Disk Encryption (LUKS, BitLocker)
    *   Database Encryption
    *   File Encryption
*   Blockchain Technology
    *   Hashing in Blockchain
    *   Digital Signatures in Transactions
    *   Cryptographic keys for wallets
*   Cloud Security
    *   Key Management in the Cloud
    *   Data Encryption in the Cloud

**IX. Cryptography Standards and Regulations**

*   NIST Standards
*   FIPS Publications
*   ISO Standards
*   HIPAA Compliance
*   GDPR Compliance

**X. Emerging Trends in Cryptography**

*   Post-Quantum Cryptography
    *   Understanding the threat of quantum computers to current cryptographic algorithms
    *   Exploring lattice-based cryptography, code-based cryptography, multivariate cryptography, hash-based cryptography
*   Homomorphic Encryption
    *   Fully Homomorphic Encryption (FHE)
    *   Partially Homomorphic Encryption (PHE)
    *   Applications of Homomorphic Encryption
*   Multi-Party Computation (MPC)
    *   Secure computation protocols
*   Zero-Knowledge Proofs
    *   Applications in authentication and privacy

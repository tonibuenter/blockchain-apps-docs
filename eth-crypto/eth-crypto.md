# Using `eth-crypto` Package

Sensitive and private data is saved using the encryption package `eth-crypto`. This is considered safe and sound for
encrypting data. For decryption, the private key is used. Unfortunately, MetaMask and other wallets do not provide this
encryption or open access to the private key. Therefore, encryption is currently reduced for the Local Wallet.

## Detailed Explanation Concerning Safety and Soundness of the `eth-crypto` Package

The `encryptWithPublicKey` function from the `eth-crypto` npm package is generally considered safe and sound due to the
underlying cryptography it employs. Here's a breakdown of why:

### 1. ECIES (Elliptic Curve Integrated Encryption Scheme)

`eth-crypto` uses ECIES for encryption. ECIES is a well-established and widely used standard for public-key encryption.
It combines the security of elliptic curve cryptography (ECC) with the speed of symmetric encryption.

**How it works:**

- A random ephemeral key pair is generated.
- The ephemeral public key is used to derive a shared secret using Elliptic Curve Diffie-Hellman (ECDH) with the
  recipient's public key.
- The shared secret is used to encrypt the message with a symmetric encryption algorithm like AES.
- The encrypted message, along with the ephemeral public key, is sent to the recipient.

### 2. Strong Encryption Algorithms

- **AES-256-CBC:** ECIES in `eth-crypto` utilizes AES-256 in CBC mode for symmetric encryption. AES is a robust and
  widely trusted encryption standard.
- **HMAC-SHA-256:** For message authentication, HMAC-SHA-256 is used. This ensures the integrity of the message and
  prevents tampering.

### 3. Secure Key Derivation

ECDH is used to securely derive a shared secret from the ephemeral key pair and the recipient's public key. This shared
secret is the foundation of the encryption process.

### 4. Open Source and Community Vetting

`eth-crypto` is an open-source project, allowing the community to review and audit the code for potential
vulnerabilities. This transparency helps ensure its security.

### Important Considerations

While `encryptWithPublicKey` is generally secure, it's crucial to use it correctly and be aware of potential risks:

- **Key Management:** The security of any encryption system relies heavily on proper key management. Protect your
  private keys and ensure they are not compromised.
- **Implementation Flaws:** While the underlying cryptography is sound, there's always a possibility of implementation
  flaws in the library itself. Stay updated with the latest versions of `eth-crypto` to benefit from any security
  patches.
- **Quantum Computing:** In the future, quantum computers could potentially break ECC. However, this is still a
  long-term concern, and post-quantum cryptography is being developed to address this threat.

**In summary,** `encryptWithPublicKey` in `eth-crypto` is considered safe due to its use of well-established
cryptographic standards and algorithms like ECIES, AES-256, and HMAC-SHA-256. However, remember to practice good key
management and stay informed about potential vulnerabilities.

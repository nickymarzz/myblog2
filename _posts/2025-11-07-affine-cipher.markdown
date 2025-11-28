---
layout: post
title: "The Affine Cipher: A Classic Cryptographic Technique"
date: 2025-11-07 00:00:00 -0000
categories: [cryptography, ciphers]
tags: [encryption, security]
---

## The Affine Cipher: A Classic Cryptographic Technique

The Affine cipher is a type of monoalphabetic substitution cipher, where each letter in an alphabet is mapped to its numeric equivalent, encrypted using a simple mathematical function, and converted back to a letter. The encryption function for a single letter is `E(x) = (ax + b) mod m`, where `x` is the numeric equivalent of the letter, `a` and `b` are the keys of the cipher, and `m` is the size of the alphabet.

### How It Works

1.  **Choose Keys:** The Affine cipher requires two keys, `a` and `b`. For the cipher to be unbreakable, `a` must be coprime with `m` (the size of the alphabet). This means that the greatest common divisor of `a` and `m` must be 1.

2.  **Encryption:** To encrypt a message, each letter is replaced by the corresponding letter determined by the encryption function. For example, if we use the English alphabet (m=26) and choose `a=5` and `b=8`, the letter 'a' (x=0) would be encrypted as `(5*0 + 8) mod 26 = 8`, which corresponds to the letter 'i'.

3.  **Decryption:** The decryption function is `D(y) = a^-1(y - b) mod m`, where `a^-1` is the modular multiplicative inverse of `a` modulo `m`. This inverse exists only if `a` and `m` are coprime.

### Example

Let's encrypt the word "hello" using the Affine cipher with `a=5`, `b=8`, and `m=26`.

*   **h** (7) -> `(5*7 + 8) mod 26 = 43 mod 26 = 17` -> **R**
*   **e** (4) -> `(5*4 + 8) mod 26 = 28 mod 26 = 2` -> **C**
*   **l** (11) -> `(5*11 + 8) mod 26 = 63 mod 26 = 11` -> **L**
*   **l** (11) -> `(5*11 + 8) mod 26 = 63 mod 26 = 11` -> **L**
*   **o** (14) -> `(5*14 + 8) mod 26 = 78 mod 26 = 0` -> **A**

So, "hello" becomes "RCLLA".

### Security

The Affine cipher is vulnerable to frequency analysis and other cryptanalytic attacks. Since it is a monoalphabetic substitution cipher, the frequency of letters in the ciphertext will be the same as in the plaintext. This makes it relatively easy to break for experienced cryptanalysts.

### Conclusion

The Affine cipher is a simple and elegant cryptographic technique that demonstrates the use of modular arithmetic in ciphers. While it is not secure enough for modern applications, it is an excellent educational tool for learning the basics of cryptography.

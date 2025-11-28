---
layout: post
title: "The Vigenère Cipher: A Polyalphabetic Substitution Cipher"
date: 2025-11-07 00:00:00 -0000
categories: [cryptography, ciphers]
tags: [encryption, security]
---

## The Vigenère Cipher: A Polyalphabetic Substitution Cipher

The Vigenère cipher is a method of encrypting alphabetic text by using a series of interwoven Caesar ciphers, based on the letters of a keyword. It is a form of polyalphabetic substitution, and was for a long time considered unbreakable.

### How It Works

1.  **Choose a Keyword:** A keyword is chosen, which determines the shifts used in the encryption. For example, if the keyword is "CAT", the shifts will be 2, 0, and 19.

2.  **Encryption:** To encrypt a message, the keyword is repeated as many times as necessary to match the length of the plaintext. Each letter of the plaintext is then shifted by the corresponding letter of the keyword. For example, if the plaintext is "HELLO" and the keyword is "CAT", the keyword would be repeated as "CATCA". The encryption would be as follows:

    *   **H** (7) + **C** (2) = 9 -> **J**
    *   **E** (4) + **A** (0) = 4 -> **E**
    *   **L** (11) + **T** (19) = 30 mod 26 = 4 -> **E**
    *   **L** (11) + **C** (2) = 13 -> **N**
    *   **O** (14) + **A** (0) = 14 -> **O**

    So, "HELLO" becomes "JEENO".

3.  **Decryption:** To decrypt the message, the same keyword is used, but the shifts are subtracted instead of added.

### The Vigenère Square

A Vigenère square, or Vigenère table, can be used to facilitate encryption. It consists of the alphabet written out 26 times in different rows, each alphabet shifted one letter to the left from the one above it, corresponding to the 26 possible Caesar ciphers.

### Security

The Vigenère cipher was considered secure for centuries. However, it was eventually broken by Friedrich Kasiski, who published his method in 1863. The key to breaking the cipher is to determine the length of the keyword. Once the length is known, the ciphertext can be treated as a series of interwoven Caesar ciphers, each of which can be broken with frequency analysis.

### Conclusion

The Vigenère cipher represents a significant step up in complexity from simple substitution ciphers. Its eventual cryptanalysis was a major milestone in the history of cryptography, paving the way for the development of more sophisticated ciphers.
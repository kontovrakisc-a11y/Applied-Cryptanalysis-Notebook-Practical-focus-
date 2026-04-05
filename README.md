Cryptographic Implementation and Cryptanalysis Suite
Overview
This repository documents my implementation of various cryptographic primitives and successful attacks on classical and modern cryptosystems. The focus is on bridging mathematical theory (Number Theory, Linear Algebra, and Group Theory) with practical computational security.

Key Implementations & Attacks
Symmetric Cryptography (AES): Developed manual implementations of the Advanced Encryption Standard (AES) internal states, including SubBytes, ShiftRows, and MixColumns.

Lattice-Based Cryptanalysis: Implemented a Gaussian Lattice Reduction algorithm to successfully recover private keys from NTRU-based systems, demonstrating proficiency in computational linear algebra.

Public Key Cryptography (RSA): Developed tools for RSA factoring attacks, modular square root calculation using the Tonelli-Shanks algorithm, and exploitation of implementation flaws such as the e=1 vulnerability.

Network Security Automation: Utilized pwntools and JSON-RPC to automate interactions with remote challenge servers for real-time cryptanalysis.

Number Theory Foundations: Implementations of the Extended Euclidean Algorithm, Chinese Remainder Theorem (CRT), and Euler’s Totient principles to solve modular arithmetic challenges.

Technologies Used
Languages: Python

Libraries: * NumPy: Computational Linear Algebra.

PyCryptodome: Symmetric and Asymmetric primitives.

Pwntools: Network interaction and server-side exploitation.

SymPy: Symbolic Mathematics and primality testing.

Context
The solutions within this suite were developed through the CryptoHack platform to explore the vulnerabilities of cryptographic implementations when the underlying mathematical assumptions are weakened or incorrectly applied.

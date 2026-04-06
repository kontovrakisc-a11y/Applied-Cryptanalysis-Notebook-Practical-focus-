#Contact for the file with solutions to the CTF Challenges!





# Cryptographic Implementation & Cryptanalysis Suite

A comprehensive collection of cryptographic primitives and cryptanalytic attacks, bridging pure mathematical theory—Number Theory, Linear Algebra, and Group Theory—with practical computational security.

---

## 1. Symmetric Cryptography: AES Implementation
A ground-up implementation of the **Advanced Encryption Standard (AES)** internal state transformations. This project focuses on the Substitution-Permutation Network (SPN) design.

* **Core Primitives:** Implementation of `SubBytes` (S-box mapping), `ShiftRows`, `MixColumns` (GF($2^8$) polynomial multiplication), and `AddRoundKey`.
* **Cryptanalysis:** Understanding the importance of diffusion and confusion in block cipher security.



---

## 2. Lattice-Based Cryptanalysis
Implementation of lattice reduction algorithms to break modern cryptographic assumptions.

* **Gaussian Lattice Reduction:** Developed a 2D lattice reduction algorithm to solve the **Shortest Vector Problem (SVP)**.
* **NTRU Recovery:** Successfully utilized lattice reduction to recover private keys from NTRU-based systems, demonstrating how high-dimensional geometry can compromise "quantum-resistant" primitives when parameters are poorly chosen.

<details>
<summary><b>View Gaussian Reduction Logic (2D)</b></summary>

Gaussian reduction is the 2D equivalent of the Gram-Schmidt process. Given a basis $(v_1, v_2)$, we iteratively subtract the projection of one vector onto the other to find the shortest basis:
1. $v_2 \leftarrow v_2 - m \cdot v_1$, where $m = \lfloor \frac{\langle v_1, v_2 \rangle}{\|v_1\|^2} \rceil$
2. If $\|v_2\| < \|v_1\|$, swap $v_1, v_2$ and repeat.
</details>



---

## 3. Public Key Cryptography: RSA & Modular Math
Exploiting mathematical vulnerabilities in the RSA cryptosystem and implementing core modular arithmetic foundations.

* **Factoring Attacks:** Automated recovery of private keys from weak primes and small public exponents ($e=3$, $e=1$).
* **Advanced Algorithms:** Implementation of the **Tonelli-Shanks** algorithm for modular square roots and the **Chinese Remainder Theorem (CRT)** for multi-point evaluation.
* **Foundations:** Efficient implementations of the Extended Euclidean Algorithm (EEA) and Euler’s Totient functions.



---

## 4. Automation & Remote Exploitation
Bridging the gap between local scripts and remote servers using modern security tooling.

* **Socket Interaction:** Used `pwntools` and `JSON-RPC` to automate real-time cryptanalysis against remote challenge servers.
* **Protocol Analysis:** Identifying and exploiting implementation flaws in network-layer cryptographic handshakes.

---

## Technical Stack
* **Python 3.x**
* **NumPy:** High-performance linear algebra for lattice operations.
* **PyCryptodome:** Standardized symmetric and asymmetric primitives.
* **Pwntools:** Network interaction and remote server exploitation.
* **SymPy:** Symbolic mathematics and primality testing.

## Context
These solutions were developed through the **CryptoHack** platform, focusing on identifying vulnerabilities when underlying mathematical assumptions—such as the hardness of integer factorization or the discrete log problem—are weakened or incorrectly implemented.

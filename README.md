# 🔐 Crypto-Core: DES Implementation (ECB & CBC)

[![Language: Python](https://img.shields.io/badge/Language-Python-3776AB?logo=python&logoColor=white)]()
[![Field: Cybersecurity](https://img.shields.io/badge/Field-Cryptography-red)]()
[![Status: Educational](https://img.shields.io/badge/Status-Complete-success.svg)]()

**Crypto-Core** is a Python-based implementation of the Data Encryption Standard (DES). This project provides a low-level look at symmetric-key block ciphers, specifically comparing the security properties of Electronic Codebook (ECB) and Cipher Block Chaining (CBC) modes.

## 🛠 Project Scope
This engine performs full bitwise manipulation to encrypt and decrypt text files. It serves as a technical demonstration of:
*   **Permutation & Substitution:** Implementing Initial/Final permutations and S-Box logic.
*   **Feistel Network:** Executing the 16-round transformation core.
*   **Mode Comparison:** Visualizing why CBC is superior to ECB for pattern-heavy data.

---

## 🔒 Encryption Modes

### 1. ECB (Electronic Codebook)
*   **Mechanism:** Encrypts each block of plaintext independently.
*   **Observation:** Identical plaintext blocks result in identical ciphertext blocks.
*   **Use Case:** Simple data structures where pattern leakage is not a primary concern.

### 2. CBC (Cipher Block Chaining)
*   **Mechanism:** Each block of plaintext is XORed with the previous ciphertext block before being encrypted.
*   **Observation:** Uses an Initialization Vector (IV) to ensure that identical plaintexts produce unique ciphertexts.
*   **Security:** Significantly more resistant to pattern-analysis attacks.

---

## ⚙️ Technical Features
*   **Custom Key Scheduling:** Generates 16 sub-keys from a single 64-bit master key.
*   **Padding Support:** Handles files of varying lengths using standard block padding techniques.
*   **File Stream Integration:** Robust file I/O for encrypting `.txt` files while maintaining data integrity.

## 🚀 Getting Started
1. **Clone:** `git clone https://github.com/khaled-kk/Crypto-Core-DES.git`
2. **Encrypt a File:**
   ```bash
   python main.py --mode cbc --action encrypt --input secret.txt --key 87654321

3. **Decrypt a File:
   ```bash
   python main.py --mode cbc --action decrypt --input encrypted.txt --key 87654321

---
*Developed by Khaled Walid*

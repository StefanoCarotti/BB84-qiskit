# BB84 Quantum Key Distribution (QKD) Simulation

## 🔑 Securing Communication with Quantum Mechanics

In the era of quantum computing, traditional cryptographic protocols face the looming threat of obsolescence. The **BB84 Quantum Key Distribution (QKD) Protocol**, pioneered by **Charles Bennett and Gilles Brassard in 1984**, offers an unbreakable method of secure communication by leveraging the fundamental principles of quantum mechanics. 

This repository contains a simulated implementation of the BB84 protocol using **Qiskit**, IBM’s quantum computing framework. The project explores the transmission of quantum-encoded information, detection of eavesdropping attempts, and the establishment of a secure key between two parties.

---

## 🔬 Project Overview

The **BB84 protocol** is a cornerstone of **quantum cryptography**, enabling two parties (Alice and Bob) to establish a **shared secret key** over an insecure quantum channel while detecting any interference from an eavesdropper (Eve). This implementation captures:
- **Quantum Superposition and Basis Selection**: Qubits are transmitted in randomly chosen bases, ensuring a secure exchange.
- **Detection of Eavesdropping**: Any attempt to intercept the qubits disturbs their state, revealing the presence of an intruder.
- **Secure Key Generation**: Alice and Bob reconcile their measurements to extract a final secret key that is resistant to computational attacks.

The repository includes:
- `BB84.ipynb`: A step-by-step standard implementation of the BB84 QKD protocol.
- `BB84Var.ipynb`: A variant of BB84 with an eavesdropper.

---

## 🧠 How the BB84 Protocol Works

1. **Quantum Bit Preparation**: Alice randomly prepares a sequence of qubits in one of two bases (rectilinear or diagonal).
2. **Transmission to Bob**: The qubits are sent over a quantum channel.
3. **Random Basis Measurement**: Bob measures the received qubits using randomly chosen bases.
4. **Public Basis Reconciliation**: Alice and Bob compare their measurement bases over a public channel.
5. **Key Extraction**: Only measurements performed in the same basis are retained as part of the final key.
6. **Eavesdropping Detection**: If an eavesdropper (Eve) attempts to measure the qubits, the disturbance introduces detectable errors in the key.

---

## 🌍 Why BB84 Matters

Unlike classical encryption methods that rely on **computational difficulty assumptions**, BB84 is secured by **the laws of quantum mechanics**. The **No-Cloning Theorem** prevents an adversary from making perfect copies of qubits, and **quantum measurement disturbances** ensure that any interception attempt is revealed.

With the rise of quantum computing, classical encryption algorithms such as RSA and ECC are at risk of being broken due to **Shor’s algorithm**, which efficiently factors large prime numbers. QKD protocols like BB84 are among the **only known cryptographic methods that remain secure against quantum attacks**, making them a crucial component of the future of cybersecurity.

---

## 🔍 Key Features of This Simulation

- **Quantum Key Exchange with and without an Eavesdropper**: 
  - Alice and Bob communicate securely in an ideal scenario.
  - Eve attempts to intercept, altering quantum states and triggering detection.
- **Local and Cloud-Based Simulations**:
  - Classical simulation using `qasm_simulator`.
  - Quantum execution using IBM’s `ibmqx2` backend.
- **Detailed Key Reconciliation and Error Analysis**:
  - Basis comparison.
  - Error rates when an eavesdropper is present.
  - Final key extraction and security verification.

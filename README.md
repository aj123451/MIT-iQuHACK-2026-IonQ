# ⚛️ MIT iQuHACK 2026 - IonQ Quantum Networking Challenge

This repository contains the solution developed by team **Quantum Verse** for the challenge proposed by **IonQ** during **MIT iQuHACK 2026**, one of the world's most prestigious quantum computing hackathons organized by the Massachusetts Institute of Technology.

## 🎯 The Challenge
The challenge consisted of a competitive, *Risk*-style strategy game based on quantum networking physics. The goal was to conquer nodes (cities) around the world by establishing quantum entanglement links. 

The main hurdle was **quantum noise**. The "raw" Bell pairs suffered from low fidelity due to network interference (bit-flip and phase-flip errors). To claim a high-difficulty link, we had to reach a transmission fidelity greater than **0.90**, all while managing a very strict quantum resource budget.

## 🚀 Our Solution: Entanglement Distillation
We developed error-correction algorithms using adaptive **LOCC** (Local Operations and Classical Communication) protocols. Instead of relying on resource-heavy standard methods, we designed highly efficient strategies:

### 1. "Phase Protection" Strategy (2 Bell Pairs)
A highly optimized circuit for links where Phase (Z) noise was predominant. 
* We used Hadamard gates and a sacrificial pair as a "flag" via bilateral CNOT gates.
* If the measurement of the sacrificial pair indicated the correct parity (`flag = 0`), the target pair collapsed into a high-purity state.
* **Result:** Conquered Difficulty 3 nodes (e.g., Moscow) while spending half the resources compared to competing teams.

### 2. "The X+Z Tank" Strategy (3 Bell Pairs)
For critical nodes where the noise was mixed or unknown, we implemented a complete cleanup protocol.
* **Z Sacrifice:** A pair dedicated exclusively to detecting and filtering Phase errors.
* **X Sacrifice:** A pair dedicated to detecting and filtering Bit-flip errors.
* **Result:** By sequentially purifying entanglement in both bases, we guaranteed the capture of the map's most valuable nodes (e.g., Minsk, Kyiv), surpassing the most demanding fidelity thresholds.

## 🛠️ Technologies Used
* **Python:** For routing logic, node analysis, and simulator API calls.
* **Qiskit:** Design, construction, and simulation of the quantum distillation circuits.
* **OpenQASM 3.0:** Circuit exporting and classical conditional control logic at the hardware level for execution on IonQ's infrastructure.

## 🏆 Key Achievements
* **Budget Optimization:** We achieved fidelities >0.90 using 2- and 3-pair strategies, maximizing our global "Claim Strength".
* **Strategic Expansion:** Developed a heuristic analysis script to identify "Utility Qubits" and "Bonus Bell Pairs" within the graph, enabling efficient expansion across Northern and Eastern Europe.

*Project developed during MIT iQuHACK (January 2026).*

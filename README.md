# 🚀 Q-Hack

## 🧠 Overview

This repository is a **notebook-first quantum computing project** covering multiple levels of complexity:

- ⚛️ Quantum Circuit Design  
- 🔀 Quantum Multiplexer (MUX)  
- 🌐 Bloch Sphere Visualization  
- 🔐 Quantum Cryptography (BB84)  
- 🧩 Quantum Processor Architecture (QRISC)  

All implementations are done using **Qiskit, QuTiP, and Python** inside Jupyter notebooks.

---

## 📂 Repository Structure

- 📄 README.md  
- 📓 Level1.ipynb  
- 📓 Level2.ipynb  
- 📓 Level3.ipynb  
- 📓 Level4.ipynb  
- 📓 Level5.ipynb  

---

# 🔹 Level 1 – Quantum Circuit Basics ⚛️

## 🧠 Description

This level focuses on **basic quantum circuit construction** using multiple qubits and gates.

---

## ⚙️ What is Done

- Create a multi-qubit circuit  
- Apply:
  - `X` gate (NOT)
  - `CX` gate (Controlled NOT)
  - `CCX` (Toffoli gate)  
- Measure qubits  

---

## 💻 Code Used

```python
from qiskit import QuantumCircuit

qc = QuantumCircuit(13, 5)

qc.x(0)
qc.cx(0, 1)
qc.ccx(0, 1, 2)

qc.measure([0,1,2,3,4], [0,1,2,3,4])
print(qc)

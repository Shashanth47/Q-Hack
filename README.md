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

---
#🔹 Level 2 – Quantum Multiplexer 🔀
##🧠 Description
This level implements a 4×1 Multiplexer (MUX) using quantum logic.
---
⚙️ What is Done
Define 4 data inputs (d0–d3)
Use 2 select lines (s0, s1)
Apply controlled gates (CCX)
Route selected input to output
💻 Code Used
from qiskit import QuantumCircuit

qc = QuantumCircuit(7, 1)

# Example inputs
qc.x(0)  # d0 = 1
qc.x(4)  # s0 = 1

# Controlled logic
qc.ccx(4, 5, 6)

qc.measure(6, 0)
print(qc)

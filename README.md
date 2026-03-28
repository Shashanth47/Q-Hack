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

python
from qiskit import QuantumCircuit

qc = QuantumCircuit(13, 5)

qc.x(0)
qc.cx(0, 1)
qc.ccx(0, 1, 2)

qc.measure([0,1,2,3,4], [0,1,2,3,4])
print(qc)
🎯 Outcome
Understand multi-qubit operations
Learn basic quantum gates
Perform measurement

---


#🔹 Level 2 – Quantum Multiplexer 🔀
🧠 Description

Implements a 4×1 Multiplexer (MUX) using quantum logic.

⚙️ Logic
s1 s0 → output
00 → d0
01 → d1
10 → d2
11 → d3
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
🎯 Outcome
Understand quantum control logic
Implement MUX using reversible gates

---

#🔹 Level 3 – Bloch Sphere Visualization 🌐
🧠 Description

Visualizes quantum states on the Bloch Sphere using QuTiP.

⚙️ What is Done
Create quantum states
Compute expectation values
Plot Bloch sphere
💻 Code Used
from qutip import basis, Bloch

b = Bloch()

zero = basis(2,0)
one = basis(2,1)

b.add_states(zero)
b.add_states(one)

b.show()
🎯 Outcome
Visual understanding of:
Superposition
Quantum states
Learn geometric interpretation




#🔹 Level 4 – BB84 Protocol 🔐
🧠 Description

Implements quantum key distribution using BB84 protocol.

⚙️ What is Done
Alice sends qubits
Eve intercepts (optional)
Bob measures
Error detection using QBER
💻 Code Used
import random

alice_bits = [random.randint(0,1) for _ in range(10)]
alice_bases = [random.randint(0,1) for _ in range(10)]
bob_bases = [random.randint(0,1) for _ in range(10)]

shared_key = []

for i in range(10):
    if alice_bases[i] == bob_bases[i]:
        shared_key.append(alice_bits[i])

print("Shared Key:", shared_key)
🎯 Outcome
Understand quantum cryptography
Learn about:
QBER (error rate)
Eve detection




#🔹 Level 5 – QRISC Processor 🧩
🧠 Description

Implements a quantum-inspired processor architecture.

⚙️ Features
8-bit instruction format
Fetch → Decode → Execute pipeline
MAC unit
Flags (Z, P, C)
Hazard detection
Branching
💻 Code Used
from qiskit import QuantumCircuit

class QRISCProcessor:
    def __init__(self):
        self.qc = QuantumCircuit(8, 8)
        self.pc = 0
        self.reg = [0]*8

    def execute(self, opcode, q1, q2, q3):
        if opcode == "00":
            self.qc.h(q1)
        elif opcode == "01":
            self.qc.x(q1)
        elif opcode == "10":
            self.qc.cx(q1, q2)

processor = QRISCProcessor()
🎯 Outcome
Understand:
Instruction decoding
Processor pipeline
Hybrid quantum-classical systems
⚙️ How to Run ▶️
pip install qiskit qiskit-aer qutip matplotlib numpy

Then open notebooks:

jupyter notebook
📊 What This Project Covers
⚛️ Quantum circuits
🔀 Combinational logic (MUX)
🌐 Visualization
🔐 Cryptography
🧩 Processor design

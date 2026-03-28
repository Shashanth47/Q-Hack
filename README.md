🎯 Outcome
Understand multi-qubit operations
Learn basic quantum gates
Perform measurement
🔹 Level 2 – Quantum Multiplexer 🔀
🧠 Description

This level implements a 4×1 Multiplexer (MUX) using quantum logic.

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
🎯 Outcome
Understand quantum control logic
Implement MUX using reversible gates
Learn selection using control qubits
🔹 Level 3 – Bloch Sphere Visualization 🌐
🧠 Description

This level visualizes quantum states on the Bloch Sphere using QuTiP.

⚙️ What is Done
Create quantum basis states
Generate superposition states
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
Visual understanding of quantum states
Understand superposition
Learn geometric representation of qubits
🔹 Level 4 – BB84 Protocol 🔐
🧠 Description

This level implements quantum key distribution using the BB84 protocol.

⚙️ What is Done
Alice generates random bits and bases
Encodes qubits
Eve may intercept (optional)
Bob measures using random bases
Compare results to generate key
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
Learn QBER (error rate)
Understand Eve detection
🔹 Level 5 – QRISC Processor 🧩
🧠 Description

This level implements a quantum-inspired processor architecture.

⚙️ What is Done
Define 8-bit instruction format
Implement Fetch → Decode → Execute pipeline
Add MAC (Multiply-Accumulate) unit
Maintain flags (Z, P, C)
Simulate hazard detection
Enable branching
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
Understand instruction decoding
Learn processor pipeline
Explore hybrid quantum-classical systems
⚙️ How to Run ▶️
pip install qiskit qiskit-aer qutip matplotlib numpy

Then run:

jupyter notebook
📊 What This Project Covers
⚛️ Quantum circuits
🔀 Combinational logic (MUX)
🌐 Visualization
🔐 Cryptography
🧩 Processor design
⚠️ Limitations
Simulation only
No real quantum hardware
MAC is classical

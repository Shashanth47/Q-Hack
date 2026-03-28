Q-Hack Repository Documentation
📌 1. Repository Overview

This repository contains multiple quantum computing experiments implemented using Qiskit and QuTiP, organized into five levels. Each notebook explores a different concept in quantum computation, ranging from basic circuit design to quantum communication and processor simulation.

📁 2. File Inventory
🔹 Level1.ipynb

Implements a 4-bit Reversible Ripple Carry Adder (RCA) using quantum gates.

Qubits: 13
Classical bits: 5
Gates used: x, cx, ccx
Purpose:
Demonstrates reversible computation
Implements binary addition using quantum logic
Measures output and verifies correctness
🔹 Level2.ipynb

Implements a quantum multiplexer-like circuit.

Qubits: 7
Gates used: x, mcx
Purpose:
Encodes selection logic using multi-controlled gates
Simulates conditional routing of quantum data
Outputs selected value via measurement
🔹 Level3.ipynb

Analyzes quantum states on the Bloch sphere using QuTiP.

States used:
ψ₁ = (|0⟩ + |1⟩)/√2
ψ₂ = (|0⟩ − |1⟩)/√2
Libraries:
basis, sigmax, sigmay, sigmaz, expect, Bloch
Purpose:
Converts quantum states to Bloch coordinates
Visualizes them on the Bloch sphere
Verifies orthogonality using inner product
🔹 Level4.ipynb

Simulates a BB84 Quantum Key Distribution protocol.

Libraries:
QuantumCircuit, Aer, random
Purpose:
Models Alice, Eve, and Bob interactions
Simulates basis selection and measurement
Demonstrates quantum security principles
🔹 Level5.ipynb

Implements a QRISC-style Quantum Processor Simulator.

Core Class: QRISCProcessor
Key Features:
Instruction execution loop
Opcode mapping
Register management
Flag handling (Z, P, C)
Purpose:
Simulates a simplified quantum instruction processor
Bridges classical architecture with quantum circuits
🧠 3. Architecture Overview

The repository follows a progressive learning structure:

Level 1 → Quantum Arithmetic
Level 2 → Quantum Control Logic
Level 3 → Quantum State Visualization
Level 4 → Quantum Communication
Level 5 → Quantum Processor Simulation

Each level builds on conceptual understanding rather than shared code dependencies.

🔄 4. Data Flow
Input → Quantum Circuit → Gate Operations → Measurement → Classical Output
Level 1 & 2: Logic-based circuit execution
Level 3: State → Bloch transformation
Level 4: Randomized protocol simulation
Level 5: Instruction → Execution → State update
⚙️ 5. State Management
Notebook-based execution (cell order matters)
Variables persist within notebook sessions
Outputs are stored alongside code (Jupyter JSON format)
Special Case: Level 5
Uses explicit state variables:
pc (program counter)
reg (registers)
Z, P, C (flags)
📦 6. Dependencies

The project uses:

qiskit
qiskit-aer
qutip
matplotlib
numpy
random (standard library)

Dependencies are directly imported in notebooks (no requirements.txt)

🎯 7. Key Highlights
Demonstrates reversible computation
Implements quantum control logic
Visualizes quantum states geometrically
Simulates quantum cryptography
Prototypes a quantum processor model

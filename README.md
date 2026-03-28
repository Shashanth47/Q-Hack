# Q-Hack


Repository Boundary and File Inventory
<img width="657" height="884" alt="image" src="https://github.com/user-attachments/assets/832b1afc-40cf-4718-81f5-68f56bcdfd8a" />

Level1.ipynb
`Level1.ipynb`
This notebook builds a QuantumCircuit(13, 5) with Qiskit, applies x, cx, and ccx operations, and measures selected qubits into classical bits. It imports QuantumCircuit, AerSimulator, transpile, and matplotlib.pyplot.
Level2.ipynb
`Level2.ipynb`
This notebook builds a QuantumCircuit(7, 1) and uses mcx gates to implement a multiplexer-style selection flow over data qubits and selector qubits. It compiles the circuit for aer_simulator and prints the sampled output for y.
Level3.ipynb
`Level3.ipynb`
This notebook uses QuTiP to create basis states, derive superposition states, compute Bloch coordinates with expectation values over sigmax, sigmay, and sigmaz, and render those vectors with Bloch.
Level4.ipynb
`Level4.ipynb`
This notebook sets up a BB84-style security simulation using Qiskit and random basis selection for Alice, Eve, and Bob. The visible code creates single-qubit circuits in a loop, applies basis choices, and targets the Aer simulator.
Level5.ipynb
`Level5.ipynb`
This notebook defines a QRISCProcessor class and drives it with a small program list and opcode_map. The processor owns its circuit state, register mirror, flags, and execution loop.
Architecture Overview
 <img width="952" height="470" alt="image" src="https://github.com/user-attachments/assets/f0cd7881-0b17-4e2a-9a54-a4c6b2379d9f" />


<img width="1573" height="618" alt="image" src="https://github.com/user-attachments/assets/8d888228-cf38-4eb3-8f48-83c6cde3ca93" />

Level1.ipynb
`Level1.ipynb`
This notebook is a Qiskit circuit construction notebook. It creates a 13-qubit circuit with 5 classical bits and applies a sequence of x, cx, and ccx gates before measuring selected qubits.
Visible dependencies
●	QuantumCircuit
●	AerSimulator
●	transpile
●	matplotlib.pyplot
Notebook role
●	Builds a gate network over several qubits.
●	Measures circuit outputs into classical registers.
●	Serves as one of the repository’s quantum logic experiments.
Level2.ipynb
`Level2.ipynb`
This notebook implements a compact multiplexer-style quantum circuit. It uses a 7-qubit circuit, prepares input and selector qubits with x, then uses mcx to drive output qubit y.
Visible dependencies
●	QuantumCircuit
●	transpile
●	Aer
Notebook role
●	Encodes a selection function with multi-controlled X logic.
●	Compiles the circuit for the Aer simulator.
●	Samples the circuit once and prints the measured output.
Level3.ipynb
`Level3.ipynb`
This notebook uses QuTiP to analyze quantum state vectors on the Bloch sphere. It creates zero and one basis states, derives psi1 and psi2, computes Bloch coordinates, and plots them.
Visible dependencies
●	basis
●	sigmax
●	sigmay
●	sigmaz
●	expect
●	Bloch
●	numpy
Notebook role
●	Converts state vectors into Bloch coordinates.
●	Prints coordinate triples for each state.
●	Displays the two vectors on a Bloch sphere.
Major data flow
<img width="1480" height="692" alt="image" src="https://github.com/user-attachments/assets/fb6e35b2-bcd6-4ff8-a352-3dee51c36a38" />

Level4.ipynb
`Level4.ipynb`
This notebook models a BB84-style security scenario. The visible code generates random Alice bits, Alice bases, Eve bases, and Bob bases, then steps through a loop that builds one-qubit circuits and uses the Aer simulator.
Visible dependencies
●	QuantumCircuit
●	transpile
●	Aer
●	random
Notebook role
●	Models bit preparation and basis selection.
●	Uses random basis choices to simulate an interception-style workflow.
●	Collects Bob-side measurement results from the simulator.
Level5.ipynb
`Level5.ipynb`
This notebook defines the repository’s only visible class, QRISCProcessor. It also defines a small instruction stream in program and an opcode_map that maps 2-bit opcodes to operations.
Visible notebook-level data
●	program: a list of 8-bit instruction strings
●	opcode_map: a map from 2-bit opcode prefixes to instruction names


<img width="659" height="860" alt="image" src="https://github.com/user-attachments/assets/3e20cc8e-48a5-4842-bb6c-52c34e8dcab1" />


<img width="662" height="585" alt="image" src="https://github.com/user-attachments/assets/187287f3-993c-4124-b232-5462365c60b5" />


QRISCProcessor
QRISCProcessor owns the circuit and execution state for the QRISC-style prototype.
Properties
State Management
The repository’s state model is notebook-local and execution-order driven.
●	In Level1.ipynb, Level2.ipynb, Level3.ipynb, and Level4.ipynb, variables created in earlier cells are used by later cells in the same notebook session.
●	In Level5.ipynb, QRISCProcessor maintains explicit internal state through pc, reg, last_used, Z, P, and C.
●	The notebook JSON stores execution outputs alongside the source cells, which makes the saved files part code and part run record.
Dependencies
The uploaded notebooks use a small set of runtime dependencies:
●	qiskit
●	qiskit-aer
●	qutip
●	matplotlib
●	numpy
●	random from the Python standard library
These dependencies appear directly in the notebook cells rather than in a separate dependency manifest in the repository root.

<img width="1474" height="789" alt="image" src="https://github.com/user-attachments/assets/e8605574-87ff-4e6a-87ca-5d8f74c4baa5" />

<img width="659" height="771" alt="image" src="https://github.com/user-attachments/assets/55b45338-19c9-4cbb-a741-ca9eb927c513" />


# Quantum_ckts
QGSS'25
# Qiskit Global Summer School 2025: Completed Coursework 🎓

This repository contains my completed programming exercises from the Qiskit Global Summer School 2025. The coursework provides a comprehensive, hands-on journey through quantum computing, covering the spectrum from foundational principles to advanced topics in quantum error correction.

---

## Core Concepts & Technical Implementations 🚀

This curriculum is structured to build a strong theoretical and practical foundation in quantum computing using Qiskit. The key technical areas covered are detailed below.

### I. Quantum Fundamentals & Circuit Design ⚛️
This section covers the foundational principles of creating, simulating, and executing quantum circuits.
- **Circuit Construction**: Building multi-qubit quantum circuits using `QuantumCircuit`.
- **Quantum Gates**: Applying fundamental single-qubit (H, X, Z) and multi-qubit (CNOT) gates to manipulate qubit states.
- **Entanglement**: Generating and verifying canonical entangled states, including 2-qubit **Bell states** and multi-qubit **GHZ states**.
- **Simulation & Measurement**: Executing circuits on the `AerSimulator` and interpreting measurement outcomes from probability histograms.

### II. Quantum Algorithm Implementation 🔎
This section focuses on the practical implementation of a cornerstone quantum algorithm.
- **Grover's Search Algorithm**: Executing an end-to-end implementation of Grover's algorithm. This involved:
    - **Oracle Construction**: Designing a problem-specific quantum oracle to recognize and phase-shift a "marked" state.
    - **Amplitude Amplification**: Building the **diffuser** operator to selectively amplify the amplitude of the marked state, making it measurable.

### III. Hardware-Level Noise & Error Management 🛡️
This section provides hands-on experience with running circuits on real IBM Quantum hardware and implementing state-of-the-art techniques to manage noise.
- **Noise Characterization**: Quantifying the primary sources of noise in a quantum processor by experimentally measuring qubit **T1 (relaxation)** and **T2 (dephasing)** times.
- **Error Suppression**: Actively suppressing errors during computation by applying **Dynamical Decoupling** pulse sequences (specifically, the Hahn echo) to extend qubit coherence.
- **Error Mitigation**: Improving the accuracy of final results by using **Zero-Noise Extrapolation (ZNE)** via the **T-REx** library. This involves running experiments at scaled noise levels to infer the ideal, zero-noise outcome.

### IV. Quantum Error Correction (QEC) ✅
The final section is a deep dive into the theory and implementation of quantum error correction codes.
- **Stabilizer Formalism**: Working with stabilizer generators and performing **syndrome measurements** to detect the presence of errors without disturbing the encoded logical state.
- **Code Implementation & Decoding**:
    - **Steane Code**: Building a lookup-table based decoder for the `[[7,1,3]]` Steane code to correct any single-qubit error.
- **Advanced Surface Codes**:
    - **Parity Check Matrices**: Programmatically generating the complete `Hx` and `Hz` **parity check matrices** for a `12x6` lattice.
    - **Toric Code**: Implementing the nearest-neighbor toric code, a foundational surface code.
    - **Gross Code**: Constructing the Gross code, an advanced code featuring non-local, long-range stabilizer connections.
- **Code Analysis**: Calculating the number of encoded logical qubits ($k$) for the implemented codes using the formula **k = n - rank(Hx) - rank(Hz)**, demonstrating a complete understanding of a code's properties.

---

## Repository Structure 📁

- `lab0.ipynb`: Introduction to Python and the Qiskit environment.
- `lab1.ipynb`: Quantum Circuits, Gates, and Entanglement.
- `lab2.ipynb`: Implementation of Grover's Search Algorithm.
- `lab3.ipynb`: Hardware Noise Characterization, Suppression, and Mitigation.
- `lab4.ipynb`: Quantum Error Correction: Steane, Toric, and Gross Codes.

---

## How to Run ⚙️

1.  Clone the repository:
    ```bash
    git clone https://github.com/elpantherd/Quantum_ckts.git
    ```
2.  Navigate to the directory and set up a Python virtual environment.
3.  Install the required dependencies:
    ```bash
    pip install qiskit qiskit-ibm-provider numpy matplotlib notebook
    ```
4.  Launch Jupyter Notebook:
    ```bash
    jupyter notebook
    ```
5.  Open any of the `.ipynb` files to view the code and results.

---

## Acknowledgments
This coursework was developed by the IBM Quantum team for the **Qiskit Global Summer School 2025**.

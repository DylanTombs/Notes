 --- 
## Overview
- Quantum computing is an active research field with multiple competing technologies

## Annealer Technology (D-Wave)
**Key Features:**
- Uses qubits with many couplers
- Focuses on optimisation problems
- System settles into constraint-satisfying states

**Challenges:**
- No known error correction method
- Requires extremely low temperatures
- Scalability remains unproven

## Ion Traps
**How It Works:**
- Electromagnetic traps hold individual atomic ions
- Electron states used for computation
- Manipulated with microwaves/lasers

**Advantages:**
- High fidelity gates
- Clean atomic properties

**Challenges:**
- Scaling to many ions
- Requires complex vacuum systems
- Current systems limited to dozens of ions

## Neutral Atoms

![[Screenshot 2025-07-16 at 19.30.11.png]]

**Key Features:**
- Trapped with lasers (no physical hardware)
- "Egg carton" potential wells
- Atoms can be rearranged into dense grids

**Advantages:**
- Current leader in qubit counts (hundreds)
- Flexible architecture

**Challenges:**
- Measurement destroys quantum state
- Requires continuous atom reloading
- Speed limitations


## Photonic Quantum Computing
**Approach:**
- Uses single photons on photonic chips
- Probabilistic entanglement building
- Successes routed, failures discarded

**Challenges:**
- Photon loss issues
- Need for rapid photon routing/switching
- Scaling requires many components

## Quantum Dots
**Implementation:**
- Electrodes trap single electrons
- Electron states represent data

**Current Status:**
- State-of-the-art: ~12 electrons
- 1D arrays currently limiting

**Key Challenge:**
- Needs 2D arrays for fault tolerance
- Qubit failures create separate systems

## Superconducting Qubits

![[Screenshot 2025-07-16 at 19.39.39.png]]

**Design:**
- Millimeter-scale circuits on silicon wafers
- Analogous to tunable guitar strings
- States: |0⟩ (ground), |1⟩ (excited), |2⟩ (harmonics)

**Requirements:**
- Extreme cooling (~10mK)
- Microwave control systems
- Shielding from noise

**Challenges:**
- Josephson junction sensitivity
- Manufacturing yield improvements
- Preventing state leakage (|2⟩, |3⟩ etc.)

## Common Themes
- Quantum systems require large support infrastructure
- Most current implementations have <100 qubits
- Error correction remains key challenge
- No clear "winner" among technologies yet

## Classical vs Quantum Bits
**Classical Bits:**
- Fixed 0 or 1 states
- Operations: addition, multiplication, logic ops, bit shifts
- Hundreds of possible manipulations

**Quantum Bits (Qubits):**
- Store complex number amplitudes for all possible states
- For N qubits: 2ᴺ complex numbers needed to represent state
- Physical interpretation remains mysterious

![[Screenshot 2025-07-16 at 19.53.43.png]]

## Basic Quantum Gates

### Bit Flip Gate (X Gate)

![[Screenshot 2025-07-16 at 19.55.44.png]]

### Phase Flip Gate (Z Gate)


![[Screenshot 2025-07-16 at 19.57.03.png]]

### Hadamard Gate (H Gate), Controlled-NOT (CNOT)


- Second application returns to basis state
- |+⟩ and |-⟩ are physically distinguishable

![[Screenshot 2025-07-16 at 19.59.39.png]]

### Controlled-Z (CZ)

![[Screenshot 2025-07-16 at 20.04.44.png]]

- Flips sign only for |11⟩ state
- Symmetric - no distinction between control/target
- Circuit symbol: vertical line connecting qubits



## Quantum Circuits

![[Screenshot 2025-07-16 at 19.59.12.png]]

![[Screenshot 2025-07-16 at 20.08.38.png]]

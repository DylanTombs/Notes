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

# Quantum Error Correction

## Classical Error Correction Primer
**Problem:**
- Bits flip with probability p per unit time
- Need reliable storage beyond 1/p time

**Solution:**
1. **Repetition Code:**
   - Store multiple copies (e.g., 5 bits)
   - Majority voting corrects single errors
   - Fails when >50% bits flip (order p³ error rate)

2. **Code Distance:**
   - Distance d = minimum flips to change logical state
   - Can correct ⌊d/2⌋ errors
   - Higher distance → exponentially suppressed errors

**Advanced Processing:**
- **Parity Check Approach:**
  - Compare bit pairs instead of direct measurement
  - Build error graph → minimum weight perfect matching
  - Identifies error locations without direct bit access
  - Equivalent to majority voting but more quantum-compatible

![[Screenshot 2025-07-16 at 20.42.53.png]]

## Quantum Error Challenges
### Hardware Imperfections:
1. **Leakage Errors:**
   - Qubits excite beyond |0⟩/|1⟩ states
   - Corrupts neighboring qubits through gates
   - Must be handled at hardware level

![[Screenshot 2025-07-16 at 20.44.54.png]]

2. **Measurement-Induced Errors:**
   - High-power readout can excite qubits
   - Tradeoff between speed and error rate
   - Multi-qubit crosstalk concerns

![[Screenshot 2025-07-16 at 20.45.17.png]]

3. **Energy Deposition:**
   - Chip at 10mK is extremely sensitive
   - Energy spikes cause temporary "heating"
   - Results in ~50% error rates for milliseconds

## Quantum Error Model

**Key Assumptions:**
1. No leakage (only |0⟩ and |1⟩ states exist)
2. Errors manifest as:
   - Single-qubit: Arbitrary 2×2 matrices
   - Two-qubit: Arbitrary 4×4 matrices
   - During initialisation/measurement

![[Screenshot 2025-07-16 at 20.47.27.png]]

![[Screenshot 2025-07-16 at 20.57.00.png]]

**Pauli Basis Decomposition:**

![[Screenshot 2025-07-16 at 20.59.14.png]]

**Tensor Product Notation:**

![[Screenshot 2025-07-16 at 21.00.51.png]]

## Error Correction Strategy
1. **Focus on X/Z Errors:**
   - Since arbitrary errors decompose into Paulis
   - Correcting X/Z handles all linear combinations

2. **Need to Detect:**
   - Bit flips (X errors)
   - Phase flips (Z errors)
   - Both (Y errors)

3. **Without:**
   - Direct state measurement (would collapse superpositions)
   - Copying states (no-cloning theorem)

**Key Insight:**
- Use ancilla qubits to extract error syndromes
- Perform parity checks analogously to classical case
- Correct based on syndrome measurements

## Foundational Quantum Error Detection Circuits

**Key Building Blocks:**
1. **Basic Measurement Circuit:**

![[Screenshot 2025-07-18 at 20.18.38.png]]

- Measures in X-basis (detects |+⟩/|-⟩ states)
- Denoted as Mₓ measurement

1. **Error Detection Prototype:**

![[Screenshot 2025-07-18 at 17.56.25.png]]

- **No errors:** Stream of 0s
- **Data qubit error:** Permanent measurement flip (0→1)
- **Measure qubit error:** Single odd measurement

## Stabilizer Circuits
### Two-Data-Qubit Detector:

![[Screenshot 2025-07-18 at 17.59.54.png]]

  
- Detects if q₁ and q₂ become different - Preserves superposition α|00⟩ + β|11⟩ 
- Cannot identify which qubit flipped


![[Screenshot 2025-07-18 at 18.06.36.png]]

### Three-Data-Qubit Version:

- **Detectors:** Pairs of consecutive measurements
- **Detection Event:** Odd parity in measurement pair

  
## Error Location Patterns
**Bit Flip Errors Create:**
1. **Vertical Pairs:** 
	   - Errors between measurement rounds
2. **Diagonal Pairs:**
	   - Errors during gate operations
	
![[Screenshot 2025-07-18 at 18.06.36.png]]

**Decoding Process:**
1. Identify all detection events (measurement changes)
2. Build error probability graph:
   - Nodes: Detection events
   - Edges: Possible error locations
   - Weights: -log(probability)
3. Apply **minimum weight perfect matching** to:
   - Pair detection events
   - Or connect to boundary (for odd counts)

## Code Properties

**Distance-3 Code Example:**
- Can correct 1 error (⌊3/2⌋)
- Fails when ≥2 errors cause:
  - Measurement double-flips (undetectable)
  - Misleading detection patterns

**Scalability:**
- Adding more qubits → higher distance
- Linear resource increase → exponential error suppression

## Phase Flip Detection

**Modified Circuit:**

![[Screenshot 2025-07-18 at 20.22.05.png]]

- Detects Z errors instead of X errors
- Uses Hadamard transforms to change basis
- Same detection principles apply

## Stabilizer Fundamentals
**Definition:**
- An operator that leaves a quantum state unchanged (`S|ψ⟩ = |ψ⟩`)
- The set of all stabilizers for a state forms its **stabilizer group**

**Single-Qubit Examples:**
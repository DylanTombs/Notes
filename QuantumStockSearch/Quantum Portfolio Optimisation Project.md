
## Overview
- Implemented quantum-classical hybrid portfolio optimization system
- Compared VQE quantum optimization against classical mean-variance approach
- Automated parameter sweep testing across asset sizes, risk profiles, and circuit depths

## Core Components

### Main Experiment Flow (`run_experiment()`)
1. Loads top N assets from CSV
2. Generates Monte Carlo portfolios
3. Runs classical optimization
4. Executes VQE optimization
5. Calculates performance metrics
6. Generates comparison visualizations

### Key Parameters
```python
num_assets = [4, 8, 12, 16]       # Number of stocks
num_portfolios = [50,100,150,200]  # Monte Carlo samples
reps = [2,3]                       # Quantum circuit depth
risk_aversion = [0.3,0.5,0.8]      # Risk preference
```

## Implementation Details

### Quantum Optimisation

```python

q_weights, result = run_vqe_portfolio_optimization_continuous(
    means, 
    cov_matrix
)
```

- **Inputs**:
    
    - `means`: Array of expected returns
        
    - `cov_matrix`: Covariance matrix of returns
        
- **Outputs**:
    
    - Optimised weights
        
    - VQE result object

## Interview Preparation

### Technical Questions

**Q: How did you map portfolio optimization to a quantum problem?**

- Formulated as quadratic programming problem
    
- Created Hamiltonian representing risk-return tradeoff
    
- Used VQE to find ground state (optimal portfolio)
    

**Q: What were the key challenges?**

1. Parameter tuning for ansatz depth
    
2. Classical-quantum data conversion
    
3. Runtime scaling with asset count
    

### Results Analysis

- Quantum solutions competitive for small asset sets (<8)
    
- Classical faster for large portfolios
    
- Quantum advantage in exploring non-convex spaces
    

### Extension Ideas

1. Hybrid quantum-classical preprocessing
    
2. Error mitigation techniques
    
3. Alternative algorithms (QAOA, quantum annealing)
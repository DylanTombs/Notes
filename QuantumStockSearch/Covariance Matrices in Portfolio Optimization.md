
## Definition
A covariance matrix measures how changes in one asset's returns correspond to changes in another's. For `N` assets, it's an `N×N` matrix where:

- **Diagonal elements**: Variance of each asset's returns (σ²)
- **Off-diagonal elements**: Covariance between asset pairs (σᵢⱼ)

## Mathematical Formulation
For returns vector **R** = [R₁, R₂, ..., Rₙ]:
```math
\Sigma_{i,j} = \text{Cov}(R_i, R_j) = \mathbb{E}[(R_i - \mu_i)(R_j - \mu_j)] 
```

## Portfolio Risk Calculation

Portfolio variance (risk) for weights **w**:

```math

\sigma_p^2 = \mathbf{w}^T \Sigma \mathbf{w} = \sum_{i,j} w_i w_j \Sigma_{i,j}
```

## Key Properties

1. **Symmetric** (Σ = Σᵀ)
    
2. **Positive semi-definite** (wᵀΣw ≥ 0)
    
3. **Correlation** can be derived:  
    ρᵢⱼ = Σᵢⱼ/(σᵢσⱼ)
    

## Visualisation
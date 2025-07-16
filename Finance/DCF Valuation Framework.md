
#finance #valuation #dcf    

---

## 1. Core Components  
### Free Cash Flow (FCF)  
- **Formula**:  
		FCF = EBIT(1 - Tax Rate) + D&A - CapEx - ΔNWC
- **Key Drivers**:  
- Revenue growth ([[Management Estimates]])  
- EBITDA margins  
- Working capital cycles  

### Discount Rate (WACC)  
- **Formula**:  
	 WACC = (E/V × Re) + (D/V × Rd × (1 - Tax Rate))
-  **Inputs**:  
- Cost of equity (`Re`): [[CAPM]]  
- Cost of debt (`Rd`): Pre-tax interest rate  
- Target capital structure (`E/V`, `D/V`)  

### Terminal Value  
- **Gordon Growth Method**:  
		TV = FCFₙ × (1 + g) / (WACC - g)
-  **Exit Multiple Method**:
		TV = EBITDAₙ × Trading Multiple


---

## Key Assumptions  
###  Management Estimates  
- **Revenue Growth**:  
- 2025E: 2% → 2030E: 1% (link to [[Revenue Model]])  
- **Margins**:  
- EBITDA: 20% → 22% (cost savings)  
- **CapEx**: 5% of revenue  

### Outside-In Extrapolation  
- **Market Comparables**:  
- Peer EV/EBITDA: 8x–12x  
- Implied growth check: 1.5% (vs. management’s 1%)  
- **Sensitivity Table**:  
| Growth/WACC | 0.5% | 1.0% | 1.5% |  
|-------------|------|------|------|  
| **5.0%**    | $X   | $Y   | $Z   |  

---

## Workflow Steps  
1. **Inputs Tab**:  
 - Link to [[Financial Model Excel]] for raw data.  
2. **FCF Calculation**:  
 - Use `=FCF_Year1` etc. in Excel.  
3. **Sensitivity Checks**:  
 - [[Scenario Analysis]] with ±1% growth/WACC.  

---

## Common Pitfalls  
-  Over-optimistic terminal growth (`g > WACC`).  
-  Ignoring cyclicality in [[Working Capital]].  
-  Mismatched WACC/FCF time horizons.  

---

## Links  

- [[LBO Model]]
- [[Trading Comps]]
- [[M&A Synergies]]  
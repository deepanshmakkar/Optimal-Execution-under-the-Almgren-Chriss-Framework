# Optimal Execution under the Almgren–Chriss Framework

This repository contains a complete implementation and analysis of the **Almgren–Chriss optimal execution model**, covering both deterministic (open-loop) and stochastic (closed-loop) formulations.

---

## Contents

### 1. Research Paper
**`Deterministic and Stochastic Optimal Execution in the Almgren–Chriss Model.pdf`**

Manuscript written in Markdown and compiled to PDF using Pandoc.  
The paper includes:

- Discrete-time deterministic Almgren–Chriss formulation  
- Convex quadratic program and KKT characterization  
- Structural invariants and TWAP comparison  
- Continuous-time limit and Euler–Lagrange equation  
- Stochastic extension via dynamic programming  
- Riccati recursion and linear state-feedback control  
- Monte Carlo validation of risk reduction  
- Economic interpretation and parameter sensitivity
  
---

### 2. Notebooks

#### `deterministic_ac.ipynb`
Implements the deterministic Almgren–Chriss model:

- Exact liquidation via equality constraint  
- Quadratic objective with temporary impact and inventory risk  
- KKT system solution  
- Inventory and trading-rate trajectories  
- Risk-aversion sensitivity analysis  
- Continuous-time convergence and discretization comparison  

#### `stochastic_ac.ipynb`
Implements the stochastic Almgren–Chriss model:

- Price dynamics with Brownian motion  
- Mean–variance execution objective  
- Dynamic programming formulation  
- Quadratic value function ansatz  
- Riccati recursion and feedback control  
- Monte Carlo simulation of execution proceeds  
- Comparison with deterministic execution  

---

## Mathematical Framework

Both models are formulated as **finite-horizon linear–quadratic control problems**:

- Deterministic execution → constrained quadratic program  
- Stochastic execution → stochastic LQR with terminal penalty  

The project highlights:
- Exact liquidation vs terminal penalties  
- Open-loop vs closed-loop execution  
- Certainty equivalence in linear–quadratic settings  
- Risk reduction through feedback control  

---

## Reproducibility

- All results are generated from the notebooks in this repository  
- Fixed random seeds are used for Monte Carlo experiments  
- No proprietary data or external APIs are required  

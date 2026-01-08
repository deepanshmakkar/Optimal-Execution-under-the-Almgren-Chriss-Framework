# Optimal Execution under the Almgren–Chriss Framework

This repository contains an implementation and analysis of the Almgren–Chriss optimal execution model in both deterministic and stochastic settings. The work treats optimal execution as a sequence of linear–quadratic control problems and focuses on derivation, structure, and numerical validation rather than heuristic trading rules.

---

## Contents

### 1. Research Manuscript
**`Deterministic and Stochastic Optimal Execution in the Almgren–Chriss Model.pdf`**

A research-style manuscript written in Markdown and compiled to PDF using Pandoc.

The manuscript covers:

- Discrete-time deterministic Almgren–Chriss formulation  
- Operator representation of inventory dynamics  
- Convex quadratic program and KKT characterization  
- Structural invariants and TWAP benchmark comparison  
- Continuous-time limit and Euler–Lagrange equation  
- Euler–Lagrange discretization and convergence analysis  
- Stochastic formulation via dynamic programming  
- Riccati recursion and linear state-feedback control  
- Monte Carlo validation of execution risk reduction  
- Parameter sensitivity and economic interpretation  

---

### 2. Notebooks

#### `deterministic_ac.ipynb`
Implements the deterministic Almgren–Chriss model:

- Exact liquidation enforced through an equality constraint  
- Quadratic objective with temporary market impact and inventory risk  
- KKT system construction and solution  
- Optimal trading-rate and inventory trajectories  
- Sensitivity analysis with respect to risk aversion  
- Cost–risk decomposition  
- Continuous-time convergence and discretization comparison  

#### `stochastic_ac.ipynb`
Implements the stochastic Almgren–Chriss model:

- Stochastic price dynamics with Brownian motion  
- Mean–variance execution objective  
- Dynamic programming formulation  
- Quadratic value function ansatz  
- Riccati recursion and linear feedback control  
- Monte Carlo comparison of open-loop and closed-loop execution  
- Estimation of volatility and temporary market impact  
- Numerical diagnostics and grid-resolution sensitivity  
- Extension to nonlinear temporary market impact using grid-based dynamic programming  

---

## Mathematical Framework

Both execution problems are formulated as finite-horizon control problems.

- Deterministic execution corresponds to a constrained quadratic program.  
- Stochastic execution corresponds to a stochastic linear–quadratic regulator with a terminal inventory penalty.

The analysis emphasizes:

- Exact liquidation versus terminal penalty formulations  
- Open-loop versus closed-loop execution strategies  
- Certainty equivalence under linear dynamics  
- Reduction of execution risk through feedback control  
- Loss of linear–quadratic structure under nonlinear market impact  

---

## Reproducibility and Numerical Validation

- All results are generated directly from the notebooks in this repository.  
- Fixed random seeds are used for Monte Carlo simulations.  
- Grid refinement and policy monotonicity are explicitly checked.  
- No proprietary data or external APIs are required.

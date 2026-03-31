# Stochastic Portfolio Engine — Python

![Python](https://img.shields.io/badge/Python-3.8%2B-blue) ![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange) ![License](https://img.shields.io/badge/License-MIT-green)

## Overview

A quantitative portfolio construction engine that automates the generation of the efficient frontier using Monte Carlo simulation, and identifies optimal asset allocations via Sharpe ratio maximisation. Built using core scientific Python libraries without reliance on dedicated finance frameworks, demonstrating full implementation from scratch.

## Key Features

- **Monte Carlo Simulation** for automated efficient frontier generation across thousands of random portfolios
- **Sharpe Ratio Optimisation** to identify the maximum risk-adjusted return portfolio
- **Efficient Frontier Visualisation** with clear plotting of risk/return trade-offs
- **Minimum Variance Portfolio** identification
- **Covariance Matrix Analysis** for realistic correlation modelling between assets

## Methodology

### 1. Data Collection
Historical price data is retrieved for a set of assets. Log returns are computed to normalise for compounding effects.

### 2. Monte Carlo Simulation
Thousands of random portfolio weight combinations are generated. For each, the expected annual return, volatility (standard deviation), and Sharpe ratio are calculated.

### 3. Efficient Frontier
The results are plotted to produce the efficient frontier — the set of portfolios offering maximum return for a given level of risk.

### 4. Optimal Portfolio
The portfolio with the highest Sharpe ratio is extracted as the optimal allocation, alongside the minimum variance portfolio.

## Technologies Used

| Tool | Purpose |
|------|---------|
| Python 3.8+ | Core language |
| NumPy | Matrix operations, random weight generation |
| Pandas | Data wrangling and return calculations |
| SciPy | Numerical optimisation |
| Matplotlib | Efficient frontier plotting |
| yfinance | Asset price data retrieval |

## Project Structure

```
├── Stochastic_Portfolio_Engine.ipynb   # Main notebook
└── README.md
```

## Sample Output

The engine produces an efficient frontier scatter plot colour-mapped by Sharpe ratio, with markers for the **optimal Sharpe portfolio** and **minimum variance portfolio**.

## Getting Started

```bash
# Clone the repository
git clone https://github.com/srhimal149/Stochastic-Portfolio-Engine-Python-.git
cd Stochastic-Portfolio-Engine-Python-

# Install dependencies
pip install numpy pandas scipy matplotlib yfinance jupyter

# Launch Jupyter
jupyter notebook
```

## Author

**Md Saifur Rahman Himal**
MSc FinTech (Distinction Candidate) | Quantitative Finance & ML
[LinkedIn](https://www.linkedin.com/in/md-saifur-rahman-himal-70a0941ba) | [GitHub](https://github.com/srhimal149)

## License

MIT License — feel free to use and adapt with attribution.

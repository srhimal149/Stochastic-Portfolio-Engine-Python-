# Stochastic Portfolio Engine — Python

![Python](https://img.shields.io/badge/Python-3.8%2B-blue) ![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange) ![License](https://img.shields.io/badge/License-MIT-green)

## Overview

A comprehensive quantitative finance notebook covering portfolio construction, CAPM analysis, Value-at-Risk, and Monte Carlo simulation applied to **SBRY.L** (Sainsbury's) and **TSCO.L** (Tesco) benchmarked against the **FTSE 100 (^FTSE)**. Data spans May 2024 – May 2025 sourced via `yfinance`.

The notebook follows a structured step-by-step approach from data loading through to optimal portfolio identification.

---

## What's Inside

### Step 1: Data Loading & EDA
- Downloads price data for SBRY.L, TSCO.L, ^FTSE using `yfinance`
- - Computes descriptive statistics and inspects data quality (269 trading days)
 
  - ### Step 2: Return & Excess Return Calculation
  - - Computes daily log/simple returns
    - - Calculates excess returns over a 4% annual risk-free rate (FRED-based): `rf_annual = 0.04`
     
      - ### Step 3: Max Drawdown Analysis
      - - SBRY max drawdown: -23.67%
        - - TSCO max drawdown: -20.76%
         
          - ### Step 4: Value at Risk (VaR)
          - Historical quantile-based VaR at two confidence levels:
          - - **VaR 95%**: SBRY -2.32%, TSCO -1.68%
            - - **VaR 99%**: SBRY -4.16%, TSCO -4.00%
             
              - ### Step 5: CAPM Analysis
              - OLS regression of excess asset returns against FTSE excess returns:
              - - Yields beta (systematic risk) and alpha (abnormal return) for each stock
               
                - ### Step 6: Monte Carlo Simulation (1,000 portfolios)
                - - Generates random Dirichlet-weighted portfolios over SBRY.L and TSCO.L
                  - - Computes expected return, volatility, and Sharpe ratio for each simulation
                    - - Identifies **Best Sharpe**, **Worst Sharpe**, and **Lowest Risk** portfolios
                     
                      - **Best Sharpe Result:**
                      - - Return: 18.4% | Volatility: 20.1% | Sharpe: 0.938
                        - - Weights: SBRY 0.4% / TSCO 99.6%
                         
                          - **Lowest Risk Result:**
                          - - Return: 18.4% | Volatility: 20.1% | Sharpe: 0.715
                            - - Weights: SBRY 34.2% / TSCO 65.8%
                             
                              - ---

                              ## Key Results

                              | Metric | SBRY.L | TSCO.L |
                              |--------|--------|--------|
                              | Expected Return (ann.) | 7.87% | 23.81% |
                              | Volatility (ann.) | 23.46% | 21.07% |
                              | VaR 95% | -2.32% | -1.68% |
                              | VaR 99% | -4.16% | -4.00% |
                              | Max Drawdown | -23.67% | -20.76% |

                              ---

                              ## Technologies Used

                              | Tool | Purpose |
                              |------|---------|
                              | Python 3.8+ | Core language |
                              | yfinance | Market data retrieval |
                              | NumPy / Pandas | Data manipulation |
                              | SciPy (stats, linregress) | CAPM regression |
                              | Matplotlib / Seaborn | Visualisations (skew, kurtosis) |
                              | Google Colab | Execution environment |

                              ## Getting Started

                              ```bash
                              git clone https://github.com/srhimal149/Stochastic-Portfolio-Engine-Python-.git
                              cd Stochastic-Portfolio-Engine-Python-
                              pip install yfinance numpy pandas scipy matplotlib seaborn jupyter
                              jupyter notebook
                              ```

                              ## Author

                              **Md Saifur Rahman Himal**
                              MSc FinTech (Distinction Candidate) | Quantitative Finance & ML
                              [LinkedIn](https://www.linkedin.com/in/md-saifur-rahman-himal-70a0941ba) | [GitHub](https://github.com/srhimal149)

                              ## License

                              MIT License

# Market Risk Analysis: Portfolio VaR & Expected Shortfall 📉💼

An advanced quantitative analysis project focused on assessing the market risk of a custom financial portfolio. The project explores, calculates, and compares the two most prominent risk metrics in the financial industry: **Value at Risk (VaR)** and **Expected Shortfall (ES)** (also known as Conditional VaR), applying different estimation methodologies to evaluate the portfolio's tail risk exposure.

## 🎯 Project Overview
The main objective of this repository is to build a diversified financial portfolio and quantify its potential losses over a specified time horizon and confidence level (e.g., 95% and 99%). The analysis implements three main approaches:
1. **Historical Simulation:** Non-parametric approach using empirical historical returns.
2. **Parametric (Variance-Covariance) Approach:** Assuming normal distribution of returns.
3. **Monte Carlo Simulation:** A robust, stochastic approach to model complex non-linear risks.

## 🎲 Focus: Monte Carlo VaR & ES
The core of this project lies in the implementation of **Monte Carlo simulations** to forecast the portfolio's P&L distribution. Unlike parametric models, the Monte Carlo engine provides the flexibility to handle complex market dynamics and non-normal asset behaviours.

### Monte Carlo Methodology implemented:
* **Stochastic Path Generation:** We simulated thousands of possible future scenarios for the portfolio assets, leveraging multivariate distributions and capturing the correlation matrix between the assets (e.g., via Cholesky decomposition).
* **Monte Carlo Value at Risk (VaR):** After generating the simulated P&L distribution, the MC VaR is extracted by identifying the $\alpha$-quantile of the simulated losses. It answers the question: *"What is the maximum expected loss under normal market conditions at a given confidence level?"*
* **Monte Carlo Expected Shortfall (ES):** To address the limitations of VaR (which ignores the severity of losses beyond the threshold), we implemented the Expected Shortfall. The MC ES is computed by averaging all the simulated portfolio losses that strictly exceed the calculated Monte Carlo VaR, providing a coherent risk measure for extreme tail events.

## 📊 Key Results & Comparisons
By implementing multiple methodologies, the project provides a comparative analysis of the risk metrics. The Monte Carlo approach is evaluated against Historical and Parametric methods to highlight differences in tail risk capture, especially during volatile scenarios.


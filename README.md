# Efficient Frontier Portfolio Optimizer

## Overview
This project implements **Modern Portfolio Theory (MPT)** to construct optimal investment portfolios using Python.

By analyzing the historical covariance of a **diversified multi-asset basket** (US equities, tech, gold, bonds, real estate, international equities, and energy), the engine combines **Monte Carlo simulation** with **analytical SLSQP optimization** to identify two critical strategies:
1. **Maximum Sharpe Ratio:** The portfolio that delivers the highest risk-adjusted return.
2. **Global Minimum Variance (GMV):** The portfolio with the absolute lowest volatility.

Assets were selected across uncorrelated classes — equities, bonds, commodities, and real estate — to ensure the efficient frontier reflects genuine diversification benefits rather than variance within a single sector.

## Key Features
* **Diversified Multi-Asset Universe:** SPY, AAPL, GLD, TLT, VNQ, EFA, XLE — spanning 7 asset classes to produce a well-conditioned covariance matrix.
* **Correlation Heatmap:** Visualises inter-asset correlations to confirm diversification is working as MPT requires.
* **Monte Carlo Simulation:** 10,000 random weight allocations map the shape of the Efficient Frontier.
* **Analytical Optimization:** `scipy.optimize.minimize` with SLSQP finds the *true* maximum Sharpe and minimum variance portfolios — not just the best of 10,000 random guesses.
* **Portfolio Weights Table:** Translates optimal points on the frontier into concrete asset allocations.

## Tech Stack
* **Python (NumPy, Pandas)** for matrix algebra and statistical modeling.
* **SciPy** for constrained convex optimization (SLSQP).
* **Seaborn / Matplotlib** for data visualization.
* **YFinance API** for historical asset pricing.

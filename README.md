# Efficient Frontier Portfolio Optimizer

## Overview
This project implements **Modern Portfolio Theory (MPT)** to construct optimal investment portfolios using Python. 

By analyzing the historical covariance of a multi-asset basket (AAPL, NVDA, MSFT, GOOGL, AMZN), the engine simulates **10,000 portfolio combinations** to identify two critical strategies:
1.  **Maximum Sharpe Ratio:** The portfolio that delivers the highest risk-adjusted return.
2.  **Global Minimum Variance (GMV):** The portfolio with the absolute lowest volatility.

## Key Features
* **Covariance Matrix Analysis:** Calculates asset correlation to identify diversification benefits.
* **Monte Carlo Optimization:** Simulates random weight allocations to map the Efficient Frontier.
* **Visual Analytics:** Generates a Scatter Plot of the Efficient Frontier, highlighting optimal vs. conservative allocation points.

## Tech Stack
* **Python (NumPy, Pandas)** for matrix algebra and statistical modeling.
* **Matplotlib** for data visualization.
* **YFinance API** for real-time asset pricing.
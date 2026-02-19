# Portfolio Optimization and CPPI

This project implements portfolio optimization techniques using the Markowitz Mean-Variance framework combined with a dynamic CPPI (Constant Proportion Portfolio Insurance) strategy in Python.

The objective is to design a risk-controlled investment portfolio tailored to pension funds, balancing capital protection and long-term performance.

---

## Project Context

This project was developed between October and December 2024 as part of an academic investment assignment targeting institutional investors (pension funds).

The strategy was built to ensure:

- Sustainable growth
- Controlled volatility
- Capital protection
- Strong risk-adjusted performance

Historical market data (2019–2023) were retrieved via the Yahoo Finance API.

---

## Academic Framework (Structured Investment Process)

The portfolio was developed following a structured investment methodology:

1. Define the target client
2. Design the investment strategy (objective, asset allocation, investment horizon)
3. Specify investment constraints (liquidity, turnover, tracking error)
4. Collect financial data (Yahoo Finance API via yfinance)
5. Construct and optimize the portfolio
6. Perform historical backtesting
7. Build and present an investment pitch deck

This structured process replicates real-world institutional asset management practices.

---

## Methodology

### 1. Data Collection
- Asset price data retrieved via `yfinance`
- Return computation and cleaning using `pandas`

### 2. Asset Universe
The portfolio was constructed using a diversified set of assets including:
- Equities (e.g., S&P 500 ETF proxy)
- Bonds
- Risk-free asset (proxy via Treasury rate)
The allocation was dynamically adjusted using the CPPI mechanism.

### 3. Mean-Variance Optimization
- Expected returns estimation
- Covariance matrix computation
- Efficient Frontier construction
- Maximum Sharpe Ratio portfolio identification

### 4. CPPI Implementation
- Dynamic allocation between risky and risk-free assets
- Multiplier-based exposure adjustment
- Floor protection mechanism

### 5. Performance Evaluation
- CAGR (Compound Annual Growth Rate)
- Annualized volatility
- Maximum drawdown
- Sharpe ratio

---

## Backtest Results (2019–2023)

- **Annualized Return (CAGR):** 31.93%
- **Annualized Volatility:** 10.68%
- **Maximum Drawdown:** -6.57%
- **Sharpe Ratio:** 1.69

The results demonstrate strong risk-adjusted performance while maintaining controlled downside exposure — consistent with pension fund investment objectives.

---

## Repository Structure

Portfolio-Optimization-and-CPPI
│
├── notebooks/        # Analysis notebooks (data, optimization, CPPI)
├── results/          # Generated reports and outputs
├── presentation/     # Final pitch deck
├── README.md
├── LICENSE

---

## Key Concepts Implemented

- Mean-Variance Optimization
- Efficient Frontier
- Sharpe Ratio Maximization
- Risk-Free Asset Allocation
- CPPI Dynamic Allocation Strategy
- Capital Protection Mechanism

---

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- SciPy
- yfinance


## Model Limitations

- Historical backtest does not guarantee future performance
- Transaction costs and slippage are not included
- Return expectations are based on historical averages
- CPPI performance depends on chosen multiplier and floor level

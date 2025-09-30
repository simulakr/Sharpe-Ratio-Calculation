# 📈 Sharpe Ratio Calculator for Trading Strategies

This project provides Python functions to calculate key performance metrics for trading strategies, focusing on the **Sharpe Ratio** for risk-adjusted return analysis. The calculations are based on a time-series of cumulative capital or portfolio value.

---

## ⭐ What is the Sharpe Ratio?

The **Sharpe Ratio** is a critical financial metric that measures the performance of an investment compared to a risk-free asset, after adjusting for its risk. Simply put, it tells you how much **excess return** you earn for every unit of **volatility** (risk) you take on.

### The Formula

$$
\text{Sharpe Ratio} = \frac{E(R_p) - R_f}{\sigma_p}
$$

* **$E(R_p)$**: Annualized Portfolio Return
* **$R_f$**: Annualized Risk-Free Rate
* **$\sigma_p$**: Annualized Standard Deviation (Volatility) of Portfolio Returns

### Interpretation

| Sharpe Ratio Value | Performance Assessment |
| :--- | :--- |
| **< 1.0** | Suboptimal / Average (Returns don't justify the risk) |
| **1.0 - 1.99** | Good / Acceptable |
| **$\ge$ 2.0** | **Excellent / Superior** (Strong risk-adjusted returns) |

---

## 🚀 Key Metrics Calculated

The provided Python code calculates the following essential performance metrics based on your trade results (`Capital` and `Time` columns):

1.  **Sharpe Ratio**: The primary measure of risk-adjusted returns.
2.  **Maximum Drawdown (MDD)**: The largest peak-to-trough decline during a specific period, expressed as a percentage. This represents the biggest loss an investor would have endured.
3.  **Maximum Drop Unit**: The largest peak-to-trough decline, expressed in absolute currency units (e.g., \$5,000).
4.  **Recovery Time**: The duration required for the cumulative capital to return to its previous peak value after experiencing the Maximum Drawdown.

---

## 💻 Usage: Python Code Example

You will need the `pandas` and `numpy` libraries. The core function relies on a DataFrame with a `Time` column (datetime objects) and a `Capital` column (cumulative P&L).

### Requirements

```bash
pip install pandas numpy

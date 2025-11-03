# Python Trading & Probability Experiments

---

## Repository Structure

### 1. `notebooks/probability_experiments/`
Core concepts in code:
- **01_probability_basics.ipynb** → EV, Bayes, Conditional Prob, Binomial, Variance
- **02_statistics_basics.ipynb** → LLN, CLT, Normal Dist, CI, Covariance
- **03_risk_metrics.ipynb** → Sharpe, Sortino, Kelly, Max DD, Gambler’s Ruin
- **04_simulations_and_monte_carlo.ipynb** →  progressing equity curves, 10k-path outcome distributions

### 2. `notebooks/trading_analyses/`
Real strategies + analysis:
- **btc_eth_analysis.ipynb** → BTC vs ETH: returns, vol, drawdowns
- **btc_alpha_strategy.ipynb** → 3x2 EMA strategy + Vol filter, Grid search, Positive alpha
- **ES_NQ_opening_range_breakout.ipynb** → Intraday Breakout strategy on ES/NQ (2010–2025): ORB + VWAP ensemble, Monte Carlo + K-fold Cross Validation

---

## Tools
- **Python**, **Pandas**, **NumPy**, **Matplotlib**
- **yfinance**, **DataBento** (1-min data)
- **Cursor** (strategy dev)

---

> **Code that thinks in expected value.**

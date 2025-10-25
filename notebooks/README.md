# Python-Trading-Probability
### Python projects for financial data analysis and probability experiments

A collection of Python projects for financial data analysis, probability experiments, and trading strategies / analysis.  
This repository is structured into two main areas: probability/statistics experiments and trading/analysis projects.

---

## 📂 Folder Structure

### **1. Probability Experiments** (`probability_experiments/`)  
Notebooks demonstrating basic concepts in probability and statistics:  

- [01_probability_basics.ipynb](probability_experiments/01_probability_basics.ipynb)  
  Covering Expected Value, Independent Events, Complement Rule, Binomial Probability, Conditional Probability, Bayes Theorem, Variance, and Standard Deviation.  

- [02_statistics_basics.ipynb](probability_experiments/02_statistics_basics.ipynb)  
  Covering Mean, Median, Variance, Standard Deviation, Covariance, Correlation, Normal Distribution, Z-scores, Confidence Intervals, Law of Large Numbers (LLN), and Central Limit Theorem (CLT).  

- [03_risk_metrics.ipynb](probability_experiments/03_risk_metrics.ipynb)  
  Covering Maximum Drawdown, Sharpe Ratio, Sortino Ratio, Kelly Criterion, and Gambler’s Ruin.  

- [04_simulations_monte_carlo.ipynb](probability_experiments/04_simulations_monte_carlo.ipynb)  
  Monte Carlo simulations, cumulative PnL visualization and the distribution of outcomes.


### **2. Trading and Analysis** (`trading_analysis/`)  
Notebooks applying probability, statistics, and risk metrics to real trading strategies:  

- [btc_eth_analysis.ipynb](trading_analysis/BTC_vs_ETH_analysis.ipynb)  
  Comparison and analysis of BTC and ETH. 

- [btc_alpha_strategy.ipynb](trading_analysis/Alpha_BTC_strategy.ipynb)  
    Alpha-generating strategy on BTC using a 3x2 EMA setup and volatility filter, with grid search optimization to find the best EMA parameters.
  
---

### Tools & Libraries 💻
- `Python`
- `Pandas`
- `NumPy`
- `Matplotlib`
- `yfinance`
- `Cursor`

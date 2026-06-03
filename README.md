# Financial Markets Research & Probability Notebooks

Self-directed research portfolio focused on financial markets, trading risk, probability, and Python-assisted strategy validation.

This repository is not a production trading system and is not financial advice. It is meant to show how I structure trading hypotheses, work with market data, test assumptions, evaluate risk, and communicate results with clear limitations.

Most code was built with Python, Pandas, NumPy, Matplotlib, Jupyter, and AI-assisted tools such as Cursor/Codex. My emphasis is on research design, market reasoning, risk interpretation, and documentation.

## What This Repo Demonstrates

- Financial market research across futures, crypto, and CFD-style instruments.
- Risk-aware analysis using returns, volatility, drawdown, Sharpe, Sortino, Kelly sizing, and Monte Carlo outcomes.
- Strategy validation through train/test splits, out-of-sample review, parameter sweeps, and robustness checks.
- Practical trading-operations thinking: data quality, setup verification, assumptions, monitoring, and escalation-ready notes.

## Repository Map

| Area | Path | Focus |
| --- | --- | --- |
| Case studies | [`case_studies/`](case_studies/) | Curated research summaries for larger projects that are better reviewed as concise write-ups than raw notebooks. |
| Trading analysis | [`notebooks/trading_analyses/`](notebooks/trading_analyses/) | Futures and crypto market studies, backtests, risk review, and strategy validation. |
| Probability experiments | [`notebooks/probability_experiments/`](notebooks/probability_experiments/) | Expected value, conditional probability, Bayes, LLN/CLT, risk metrics, and Monte Carlo simulations. |
| Notebook guide | [`notebooks/README.md`](notebooks/README.md) | Short guide to the notebook structure and best entry points. |

## Featured Studies

### NQ Microstructure Program Null

[`NQ microstructure case study`](case_studies/nq_microstructure_program_null/)

Case study summarizing a 1-minute OHLCV NQ futures research program that was intentionally closed after failing a predefined hard gate. The program screened 106 features across 8 families under a 1.5-tick cost assumption; it produced a healthy conditional pool but only 3 strong candidates against a 5-candidate requirement.

Why it matters: shows falsifiable research design, split discipline, data quality checks, cost-aware expected return thinking, and honest rejection of a weak research path.

### TQQQ Opening Range Breakout Replication

[`TQQQ ORB case study`](case_studies/tqqq_orb_replication/)

Replication/adaptation study of a 5-minute Opening Range Breakout strategy on TQQQ using Alpaca 1-minute data. The study compares H/L and ATR stop models and records unusually strong historical results with clear caveats around leverage, compounding, execution assumptions, and the need for stricter follow-up validation.

Why it matters: shows practical intraday backtesting, API-based data workflows, stop-model comparison, and careful interpretation of strong results rather than overclaiming.

### ES/NQ Intraday Opening Range Breakout

[`ES_NQ_opening_range_breakout.ipynb`](notebooks/trading_analyses/ES_NQ_opening_range_breakout.ipynb)

Research notebook using historical ES/NQ intraday futures data from 2010-2025. The study tests opening range breakout logic with VWAP and volatility filters, stop/take-profit rules, parameter sweeps, performance metrics, Monte Carlo simulation, and purged cross-validation concepts.

Why it matters: shows market-session awareness, data handling, hypothesis testing, drawdown review, and robustness thinking.

### BTC Alpha Strategy

[`btc_alpha_strategy.ipynb`](notebooks/trading_analyses/btc_alpha_strategy.ipynb)

Trend-following crypto strategy study using a 3 x 2 EMA majority-vote framework, volatility filters, grid search, train/test split, out-of-sample validation, and comparison against buy-and-hold behavior.

Why it matters: shows how I translate a discretionary trading idea into testable rules, then evaluate it through risk-adjusted metrics rather than headline return alone.

### BTC vs ETH Risk & Return Analysis

[`btc_eth_analysis.ipynb`](notebooks/trading_analyses/btc_eth_analysis.ipynb)

Comparative analysis of BTC and ETH using normalized growth, simple/log returns, volatility, Sharpe ratio, and drawdown behavior.

Why it matters: shows practical asset comparison, risk-adjusted thinking, and ability to summarize market behavior from data.

### Probability, Risk Metrics, and Monte Carlo

[`notebooks/probability_experiments/`](notebooks/probability_experiments/)

Notebook series covering expected value, conditional probability, Bayes, variance, standard deviation, covariance, correlation, LLN, CLT, confidence intervals, Sharpe, Sortino, Kelly, drawdowns, gambler's ruin, and Monte Carlo trade outcome distributions.

Why it matters: these are the building blocks behind position sizing, strategy evaluation, and decision-making under uncertainty.

## Research Principles

- Start with a clear market question before adding indicators.
- Separate in-sample and out-of-sample thinking where possible.
- Treat drawdown, variance, and trade sequencing as central risk questions.
- Use Monte Carlo simulation to understand path dependency, not just average outcomes.
- Document assumptions, limits, and failure modes instead of overclaiming.

## Tools

- Python, Pandas, NumPy, Matplotlib, Jupyter
- yfinance for public market data
- DataBento for market data workflows
- Cursor/Codex for AI-assisted implementation and research iteration

## Limitations

- These are research notebooks, not production trading infrastructure.
- Backtest results depend on assumptions, data quality, fees/slippage treatment, and regime selection.
- The notebooks are designed to demonstrate analysis process and risk thinking, not to publish live trading signals.

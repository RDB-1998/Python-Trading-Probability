# Trading Analysis Notebooks

Applied financial market studies using Python notebooks. These projects focus on turning market ideas into testable rules, reviewing risk-adjusted results, and documenting what the tests can and cannot prove.

## Projects

| Notebook | Market | Research Focus |
| --- | --- | --- |
| [`ES_NQ_opening_range_breakout.ipynb`](ES_NQ_opening_range_breakout.ipynb) | ES/NQ futures | Opening range breakout logic, VWAP/volatility filters, parameter sweeps, performance metrics, Monte Carlo simulation, and purged cross-validation concepts. |
| [`btc_alpha_strategy.ipynb`](btc_alpha_strategy.ipynb) | BTC | 3 x 2 EMA majority-vote trend strategy, volatility filter, grid search, train/test split, out-of-sample validation, and comparison with buy-and-hold behavior. |
| [`btc_eth_analysis.ipynb`](btc_eth_analysis.ipynb) | BTC/ETH | Comparative market analysis using returns, volatility, Sharpe ratio, and drawdown behavior. |

## What These Notebooks Show

- Market hypothesis framing before implementation.
- Risk-first review of returns, volatility, drawdown, and trade sequencing.
- Awareness of in-sample vs out-of-sample evaluation.
- Use of parameter sweeps and robustness checks rather than single-run conclusions.
- Ability to document trading logic, assumptions, and limitations in a way useful for trading operations and analyst workflows.

## Notes

These notebooks are exploratory research studies, not production trading systems or live trading signals. Results depend on assumptions, market regime, data quality, and execution/friction treatment.

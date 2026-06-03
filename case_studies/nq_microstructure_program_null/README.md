# NQ Microstructure Program Null Case Study

## Summary

This case study summarizes a self-directed NQ futures research program that was intentionally closed after failing a predefined hard gate.

The research question was:

> Can 1-minute OHLCV futures data, processed through a feature-family screening framework, surface enough robust intraday signal to justify building a downstream per-family ensemble after realistic retail trading costs?

The answer for this version was **no**.

That negative result is the point of the case study. The work demonstrates hypothesis framing, data quality checks, split discipline, feature screening, validation gates, and willingness to stop a research path when the evidence is not strong enough.

## Research Workflow Note

This was a literature-guided and heavily LLM-assisted research program. I selectively gathered research papers, PDFs, market microstructure concepts, and prior empirical findings, then used them as pivot points for deciding where the research should go next.

LLMs were used extensively for implementation support, debugging, cross-checking, code review, and audit-style reasoning. My role was to define the research direction, choose which sources and concepts mattered, set the validation discipline, interpret the results, and decide not to force the project into a positive conclusion when the evidence did not clear the gate.

## Research Design

| Area | Detail |
| --- | --- |
| Market | NQ futures, with ES used for cross-asset context. |
| Data | 1-minute OHLCV futures data, 2010-2025. Raw data is not included in this repository. |
| Cost assumption | 1.5 ticks all-in retail cost. |
| Feature set | 106 features across 8 families. |
| Families | Drift, mean reversion, volatility state, range/breakout structure, volume/participation, time of day, NQ-vs-ES cross-asset features, and order-flow toxicity proxies. |
| Labeling | Triple-barrier labels across 5, 15, and 30 minute horizons. |
| Validation discipline | Chronological split design with embargo and held-out validation/holdout periods. |

The program was planned as a 28-section pipeline. Sections 1-19 were built and validated. Sections 20-28 were intentionally not built because the candidate pool failed the hard gate before downstream ensemble construction.

## Gate Result

The key hard gate required:

| Requirement | Result | Status |
| --- | ---: | --- |
| Strong candidates | 3 / 5 required | Fail |
| Conditional candidates | 44 / 5 required | Pass |
| Families represented | 8 / 4 required | Pass |

Final result: **hard gate failed**.

The downstream validation, DSR, and holdout gates were not touched. This preserved the epistemic value of those splits for a future version rather than forcing a weak version through the pipeline.

## Main Finding

The version-1 constraint set did not surface enough robust signal:

- 1-minute OHLCV bars likely remove too much microstructure information.
- 1.5-tick retail cost was a major binding constraint.
- The strongest candidates clustered in tail-volatility mean-reversion rather than forming a diverse multi-family signal set.
- The conditional pool was healthier than the strong pool, especially in higher-volatility regimes.

This suggested that the research direction might need different constraints rather than more parameter tuning: lower effective costs, richer order-book/trade data, broader cross-asset structure, or a different labeling methodology.

## Selected Diagnostics

### Regime Distribution By Split

![Session and intraday regime distribution by split](assets/regime_distribution_by_split.png)

This chart helped confirm that regime composition changed materially across chronological splits. That matters because a candidate that looks good in one volatility environment may not generalize across later market regimes.

### Label Distribution

![Triple-barrier label distribution](assets/label_distribution.png)

The label distribution helped check whether the triple-barrier setup produced usable forward outcomes across horizons instead of a degenerate or badly imbalanced target.

### Regime-Conditional Candidate Heatmap

![Best bucket expected return by volatility regime](assets/regime_heatmap_top40.png)

The heatmap shows that many candidate effects were regime-conditional rather than stable across all regimes. This supported the conclusion that the surfaced signal was conditional, not strong enough in aggregate.

## What This Demonstrates

- Building a research process around falsifiable gates instead of open-ended optimization.
- Handling data quality, session filtering, roll logic, early-close days, and event-day calendar issues.
- Separating development, validation, and holdout logic.
- Thinking about expected return after cost, not just raw statistical pattern.
- Using LLMs as implementation and audit tools while keeping the research framing and stop/go decision evidence-driven.
- Reporting a failed research program clearly instead of overclaiming.

## What This Does Not Claim

- It does not claim a live trading edge.
- It does not publish a production trading system.
- It does not include raw data, credentials, or private working artifacts.
- It does not prove that NQ futures are untradeable; it only rejects this specific version-1 research design under the stated constraints.

## Why I Kept It In The Portfolio

Many trading projects only show successful-looking equity curves. This case study is included because disciplined rejection is part of real research. The practical skill shown here is not just coding a backtest, but knowing when the evidence is insufficient and preserving clean held-out data for future work.

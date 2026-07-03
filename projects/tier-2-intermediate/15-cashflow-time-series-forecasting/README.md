---
title: Project 15 — Time-Series Forecasting for Cash Flow
purpose: Forecast short-term cash flow for treasury/liquidity planning.
owner: Arulkumaran
dependencies: [docs/engineering-standards/machine-learning.md]
related_documents: []
version: 0.1.0
last_updated: 2026-07-02
---

## Status: **Blueprint only** — not started

## Business Problem
Forecast near-term cash inflow/outflow to support treasury liquidity planning decisions.

## Planned Architecture
Baseline naive/seasonal forecast, compared against ARIMA/Prophet and a gradient-boosted regression-on-lag-features approach.

## Planned Tech Stack
Python, statsmodels, Prophet, scikit-learn.

## Target Metric
MAPE against the naive baseline — the honest-reporting standard applies here too: a forecast that barely beats naive should be reported as such.

## Next Steps
Source or simulate a cash-flow time series.

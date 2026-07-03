---
title: Project 05 — Stock Price Movement Classification
purpose: Classify next-day directional price movement as a foundational time-series ML exercise.
owner: Arulkumaran
dependencies: [docs/engineering-standards/machine-learning.md]
related_documents: [templates/ml-pipeline-template.md]
version: 0.1.0
last_updated: 2026-07-02
---

## Status: **Blueprint only** — not started

## Business Problem
Classify whether a stock's price will move up or down the next trading day, as a foundational (not trading-signal-grade) ML exercise.

## Planned Approach
Baseline majority-class predictor, then technical-indicator features into a classifier. Explicitly framed as a learning exercise, not a trading strategy claim.

## Planned Tech Stack
Python, pandas, scikit-learn, yfinance (or similar) for data.

## Target Metric
Accuracy vs. majority-class baseline, explicitly honest about the near-random-walk nature of the problem.

## Next Steps
Source dataset, scaffold per folder-structure standard.

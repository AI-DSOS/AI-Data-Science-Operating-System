---
title: Project 24 — Real-Time Market Risk Dashboard with Streaming Data
purpose: A streaming-data dashboard for market risk metrics, demonstrating real-time system design beyond batch ML.
owner: Arulkumaran
dependencies: [docs/engineering-standards/mlops.md]
related_documents: []
version: 0.1.0
last_updated: 2026-07-02
---

## Status: **Blueprint only** — not started

## Business Problem
Surface real-time market risk metrics (VaR-style exposure, concentration risk) to a risk desk as market data streams in.

## Planned Architecture
Streaming ingestion (Kafka or a simpler polling-based simulation), rolling risk metric computation, Grafana dashboard for visualization.

## Domain Context
Demonstrates real-time system design skills distinct from the batch-oriented ML projects elsewhere in the portfolio.

## Planned Tech Stack
Python, Kafka (or simulated streaming), Grafana, a time-series database (e.g. TimescaleDB).

## Target Metric
End-to-end latency from data arrival to dashboard update; correctness of risk metric computation against a known reference calculation.

## Next Steps
Decide on real vs. simulated streaming data source given data availability constraints.

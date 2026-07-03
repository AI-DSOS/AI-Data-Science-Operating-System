---
title: Project 12 — Anomaly Detection in Trading Data
purpose: Detect anomalous trading patterns (potential errors or market abuse) in time-series trading data.
owner: Arulkumaran
dependencies: [docs/engineering-standards/machine-learning.md]
related_documents: [resources/glossary.md]
version: 0.1.0
last_updated: 2026-07-02
---

## Status: **Blueprint only** — not started

## Business Problem
Flag anomalous trades (fat-finger errors, potential market abuse patterns) in a trading data stream for compliance review.

## Planned Architecture
Isolation Forest / statistical control-chart baseline on trade size, price deviation, and timing features; streaming-friendly design.

## Domain Context
MiFID II market-abuse surveillance relevance.

## Planned Tech Stack
Python, scikit-learn, pandas; Kafka considered as a stretch goal for streaming.

## Target Metric
Precision at a fixed review-capacity recall level, same framing as Project 10.

## Next Steps
Source or simulate trading tick data.

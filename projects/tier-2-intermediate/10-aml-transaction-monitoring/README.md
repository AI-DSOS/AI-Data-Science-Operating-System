---
title: Project 10 — AML Transaction Monitoring & Alert Triage
purpose: Anomaly detection for suspicious transaction patterns, with an alert-triage layer.
owner: Arulkumaran
dependencies: [docs/engineering-standards/machine-learning.md]
related_documents: [resources/glossary.md]
version: 0.1.0
last_updated: 2026-07-02
---

## Status: **Blueprint only** — not started

## Business Problem
Detect transaction patterns suggestive of money laundering and prioritize them for human investigator review — directly KYC/AML-relevant.

## Planned Architecture
Isolation Forest unsupervised baseline + rule-based flags, combined into a triage score; alert queue UI as a stretch goal.

## Domain Context
KYC/AML (see `resources/glossary.md`) — this project's framing is one of the strongest IB-relevance pieces in the portfolio.

## Planned Tech Stack
Python, scikit-learn (Isolation Forest), FastAPI for the triage API.

## Target Metric
Alert precision at a fixed investigator-capacity recall level (not raw accuracy — false alerts have real investigator-hours cost).

## Next Steps
Source or simulate a transaction dataset (real AML data isn't public — will need realistic synthetic generation).

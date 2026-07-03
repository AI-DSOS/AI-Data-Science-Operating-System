---
title: Project 19 — Intelligent Defect Classification and Root Cause Prediction
purpose: Flagship project — classifies defects and predicts likely root cause, drawing directly on the QA automation background.
owner: Arulkumaran
dependencies: [docs/engineering-standards/mlops.md]
related_documents: [templates/ml-pipeline-template.md]
version: 0.5.0
last_updated: 2026-07-02
---

## Status: **Scoped** — architecture and roadmap designed prior to this repo; implementation in progress

## Business Problem
Classify software defects and predict their likely root cause category, directly leveraging 20+ years of QA automation domain knowledge as a genuine data advantage over typical DS candidates.

## Architecture (already designed)
Full MLOps stack matching Project 18 (MLflow, Prometheus, Grafana, Kubernetes, FastAPI) — the two flagship projects share infrastructure patterns deliberately, so lessons transfer between them.

## Domain Context
This is the clearest "QA background as competitive advantage" project in the portfolio — the training data intuition comes directly from real QA automation experience.

## Tech Stack
Python, MLflow, Prometheus, Grafana, Kubernetes, FastAPI.

## Next Steps
Migrate existing architecture documents into `docs/adr/`; begin implementation.

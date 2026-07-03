---
title: Project 09 — Real-Time Transaction Fraud Detection API
purpose: A served, monitored fraud-scoring API — first project requiring full MLOps deployment.
owner: Arulkumaran
dependencies: [docs/engineering-standards/mlops.md, docs/engineering-standards/fastapi.md]
related_documents: [templates/deployment-template.md, templates/monitoring-template.md]
version: 0.1.0
last_updated: 2026-07-02
---

## Status: **Blueprint only** — not started

## Business Problem
Score incoming transactions for fraud risk in real time, exposed as an API a bank's transaction pipeline could call.

## Planned Architecture
FastAPI service, model served from MLflow registry, containerized, deployed to Kubernetes, monitored via Prometheus/Grafana per `docs/engineering-standards/mlops.md`.

## Planned Tech Stack
Python, FastAPI, MLflow, Docker, Kubernetes, Prometheus, Grafana.

## Target Metric
p95 latency < 200ms per prediction (per `docs/engineering-standards/performance-and-scalability.md`), ROC-AUC as the model quality metric.

## Next Steps
Builds on Project 02 (Credit Card Fraud Detection) model — scaffold once that baseline model exists.

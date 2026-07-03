---
title: Project 20 — End-to-End MLOps Fraud Detection Platform
purpose: The most advanced fraud project — combines Projects 02 and 09 into a full production platform with retraining automation.
owner: Arulkumaran
dependencies: [docs/engineering-standards/mlops.md]
related_documents: []
version: 0.1.0
last_updated: 2026-07-02
---

## Status: **Blueprint only** — not started, depends on Projects 02 and 09

## Business Problem
A complete fraud detection platform: ingestion, feature store, model serving, monitoring, and automated retraining — the capstone that demonstrates full MLOps maturity, not just a served model.

## Planned Architecture
Extends Project 09's serving layer with: a feature store, drift-triggered automated retraining, and a full CI/CD pipeline from model training to production promotion.

## Planned Tech Stack
Python, FastAPI, MLflow, Kubernetes, Prometheus, Grafana, a feature store (Feast or similar).

## Target Metric
Full production checklist (`templates/production-checklist-template.md`) passed, not just a single model metric.

## Next Steps
Sequenced last among fraud-related projects — build once Projects 02 and 09 exist.

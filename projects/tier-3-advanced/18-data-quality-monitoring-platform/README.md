---
title: Project 18 — AI-Powered Data Quality Monitoring and Anomaly Detection Platform
purpose: Flagship project — full MLOps platform monitoring data quality and flagging anomalies in real time.
owner: Arulkumaran
dependencies: [docs/engineering-standards/mlops.md]
related_documents: [templates/monitoring-template.md, templates/deployment-template.md]
version: 0.5.0
last_updated: 2026-07-02
---

## Status: **Scoped** — architecture and roadmap designed prior to this repo; implementation in progress

## Business Problem
Monitor incoming data pipelines for quality issues and anomalies in real time, surfacing them before they corrupt downstream models or reports.

## Architecture (already designed)
Full MLOps stack: MLflow (experiment/model tracking), Prometheus + Grafana (monitoring), Kubernetes (deployment), FastAPI (serving). 12-week implementation roadmap already produced, along with interview Q&A preparation material built around this project.

## Domain Context
Data quality validation — one of the three flagship domains (alongside Fraud Detection and Anomaly Detection) chosen specifically because they showcase the QA-to-DS transition advantage.

## Tech Stack
Python, MLflow, Prometheus, Grafana, Kubernetes, FastAPI.

## Next Steps
Migrate the existing 12-week roadmap and architecture documents into this project's `docs/adr/` folder; begin implementation against `docs/engineering-standards/folder-structure.md`.

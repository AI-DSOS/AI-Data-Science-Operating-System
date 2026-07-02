---
title: Engineering Standard — MLOps
purpose: Deployment, monitoring, and lifecycle standards for models that graduate from experimentation to production, matching the MLflow/Prometheus/Grafana/Kubernetes stack already scoped for flagship projects.
owner: Arulkumaran
dependencies: [AGENTS.md]
related_documents: [docs/engineering-standards/README.md, docs/engineering-standards/machine-learning.md, docs/engineering-standards/docker.md, docs/engineering-standards/fastapi.md]
version: 0.1.0
last_updated: 2026-07-02
---

## Table of Contents

- [Overview](#overview)
- [Standard](#standard)
- [Examples](#examples)
- [Checklist](#checklist)
- [References](#references)
- [Next Steps](#next-steps)

## Overview

MLOps governs everything that happens to a model after `machine-learning.md`'s standards produce a sound, honestly-evaluated one: tracking, serving, monitoring, and retraining. This is the stack already named for the Data Quality Monitoring and Defect Classification projects.

## Standard

- **Experiment tracking:** MLflow (or equivalent) for every training run — parameters, metrics, and artifacts logged, not just the final model file.
- **Model registry:** models promoted through explicit stages (e.g. `staging` → `production`), never deployed directly from a notebook or ad hoc script.
- **Serving:** via FastAPI per `fastapi.md`, containerized per `docker.md`, deployed to Kubernetes for anything beyond a local demo.
- **Monitoring:** Prometheus for metrics collection, Grafana for dashboards — minimum viable dashboard covers prediction latency, request volume, and error rate; model-quality dashboards (e.g. prediction drift) added once the project has live traffic to measure.
- **Data/model drift:** define a drift-detection check (even a simple statistical one) for any project claiming to be "production-grade" — silent drift is a common gap between portfolio projects and real production systems, and naming it explicitly is a differentiator.
- **Retraining trigger:** documented per project — scheduled (e.g. monthly) or drift-triggered, not left undefined.

## Examples

```
project/
├── src/
│   └── project_name/
│       ├── training/          # MLflow-tracked training pipeline
│       ├── serving/           # FastAPI app, Docker-packaged
│       └── monitoring/        # Prometheus metrics exporters, drift checks
├── k8s/                       # Kubernetes manifests (deployment, service, ingress)
├── mlflow/                    # local MLflow tracking config (or remote server config)
```

## Checklist

- [ ] Every training run tracked (params, metrics, artifacts)
- [ ] Model promoted through registry stages, not deployed ad hoc
- [ ] Monitoring dashboard covers latency, volume, error rate at minimum
- [ ] Drift-detection check defined
- [ ] Retraining trigger documented

## References

- `docs/engineering-standards/machine-learning.md` — what happens before this standard applies
- `docs/engineering-standards/docker.md`, `fastapi.md` — the serving layer this standard builds on

## Next Steps

- Stand up a shared MLflow tracking instance (local or lightweight remote) once the first Phase 7 project needs it.

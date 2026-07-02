---
title: Engineering Standard — Jupyter
purpose: Where and how notebooks are used in DSOS projects, and the boundary between exploratory notebook work and production code.
owner: Arulkumaran
dependencies: [AGENTS.md]
related_documents: [docs/engineering-standards/README.md, docs/engineering-standards/python.md, docs/engineering-standards/folder-structure.md]
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

Notebooks are valuable for EDA and one-off model benchmarking (e.g. the car insurance five-model comparison) but are explicitly not where production pipeline code lives. This standard draws that line clearly so projects don't quietly stay notebook-only past the point they should graduate to `src/`.

## Standard

- **Location:** all notebooks live in `notebooks/` within a project, never mixed into `src/`.
- **Naming:** `NN-short-description.ipynb` (e.g. `01-eda.ipynb`, `02-model-benchmark.ipynb`) — numbered to show intended read/run order.
- **Outputs:** clear cell outputs before committing, except for a final "results" notebook meant to be read (e.g. a benchmark summary) — otherwise diffs become unreadable and repo size balloons.
- **Graduation rule:** once logic in a notebook is stable and reused, it moves into `src/` as a proper function/module and the notebook imports it — notebooks should shrink toward orchestration + visualization over a project's lifetime, not stay as the source of truth.
- **No hidden state:** a notebook should run top-to-bottom after "Restart & Run All" without errors before being considered done for a milestone.

## Examples

```
project/
├── notebooks/
│   ├── 01-eda.ipynb
│   ├── 02-model-benchmark.ipynb
│   └── 03-results-summary.ipynb   # outputs kept, meant to be read
├── src/
│   └── project_name/
│       ├── features.py            # logic graduated out of 01-eda.ipynb
│       └── models.py              # logic graduated out of 02-model-benchmark.ipynb
```

## Checklist

- [ ] Notebooks live in `notebooks/`, numbered
- [ ] Outputs cleared before commit (except intentional results notebooks)
- [ ] Reused logic graduated to `src/`
- [ ] Notebook runs clean top-to-bottom before milestone sign-off

## References

- `docs/engineering-standards/python.md` — where graduated logic ends up
- `docs/engineering-standards/folder-structure.md`

## Next Steps

- None currently.

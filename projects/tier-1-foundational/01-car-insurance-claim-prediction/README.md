---
title: Project 01 — Car Insurance Claim Prediction
purpose: Binary classification of car insurance claims under significant class imbalance.
owner: Arulkumaran
dependencies: [docs/engineering-standards/machine-learning.md]
related_documents: [templates/ml-pipeline-template.md, trackers/project-tracker.md]
version: 1.0.0
last_updated: 2026-07-02
---

## Status: **Complete** (implemented prior to DSOS repo; blueprint backfilled here)

## Business Problem
Predict which car insurance claims are likely to be filed/fraudulent, to support underwriting and claims triage decisions.

## Approach
Benchmarked five modeling strategies against a binary classification target with significant class imbalance.

## Honest Result
Class-weighted Random Forest achieved **ROC-AUC ~0.65** on held-out test data, against an aspirational target of 0.80. The gap reflects genuine class overlap in the available features, not a tuning shortfall — none of the five strategies benchmarked exceeded this ceiling. Reported transparently rather than over-tuned to look better.

## Tech Stack
Python, scikit-learn, pandas. Delivered as Word report, PowerPoint deck, Python scripts, README.

## Deliverables (already produced, outside this repo)
Word report, PowerPoint deck, Python scripts, README — not yet migrated into this repo's `src/`/`docs/adr/` structure.

## Next Steps
Migrate existing scripts into the standard folder structure (`docs/engineering-standards/folder-structure.md`) if this project is chosen as a portfolio anchor piece.

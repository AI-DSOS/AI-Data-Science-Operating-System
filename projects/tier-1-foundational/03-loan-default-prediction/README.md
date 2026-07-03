---
title: Project 03 — Loan Default Prediction
purpose: Predict borrower default risk to support credit decisioning.
owner: Arulkumaran
dependencies: [docs/engineering-standards/machine-learning.md]
related_documents: [templates/ml-pipeline-template.md]
version: 0.1.0
last_updated: 2026-07-02
---

## Status: **Blueprint only** — not started

## Business Problem
Estimate probability of loan default at application time to inform underwriting.

## Planned Approach
Logistic regression baseline with explicit threshold-shifting analysis (ties to the completed regression sprint sessions), compared against gradient-boosted trees.

## Domain Context
Basel III capital adequacy relevance — credit risk models are directly regulatory-relevant.

## Planned Tech Stack
Python, scikit-learn, XGBoost.

## Target Metric
ROC-AUC, plus a calibration check (predicted probabilities vs. actual default rates).

## Next Steps
Source dataset, scaffold per folder-structure standard.

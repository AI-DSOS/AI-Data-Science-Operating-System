---
title: Project 02 — Credit Card Fraud Detection
purpose: Classic imbalanced binary classification portfolio project establishing fraud-detection fundamentals.
owner: Arulkumaran
dependencies: [docs/engineering-standards/machine-learning.md]
related_documents: [templates/ml-pipeline-template.md]
version: 0.1.0
last_updated: 2026-07-02
---

## Status: **Blueprint only** — not started

## Business Problem
Flag likely-fraudulent credit card transactions in near real time to minimize financial loss while limiting false-positive customer friction.

## Planned Approach
Baseline (logistic regression) → SMOTE-balanced ensemble models (LightGBM/XGBoost) → SHAP explainability layer, per `docs/engineering-standards/machine-learning.md`.

## Domain Context
Directly relevant to KYC/AML-adjacent fraud monitoring functions in IB/FinTech.

## Planned Tech Stack
Python, scikit-learn, imbalanced-learn (SMOTE), LightGBM, SHAP.

## Target Metric
ROC-AUC and precision-recall trade-off explicitly discussed (false negative vs. false positive cost asymmetry).

## Next Steps
Source dataset (see `prompts/research/dataset-sourcing.md`), then scaffold per `docs/engineering-standards/folder-structure.md`.

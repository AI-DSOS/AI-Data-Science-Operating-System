---
title: Engineering Standard — Machine Learning
purpose: Baseline practices for model development across DSOS projects — experiment structure, evaluation, and honest reporting.
owner: Arulkumaran
dependencies: [AGENTS.md]
related_documents: [docs/engineering-standards/README.md, docs/engineering-standards/mlops.md, docs/departments/enterprise-project-architect.md]
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

This standard governs how models get built and evaluated, distinct from `mlops.md` (how they get deployed/monitored) and `machine-learning.md`'s own scope stops at "is this a sound, honestly-evaluated model" — deployment concerns live elsewhere.

## Standard

- **Baseline first:** every project starts with a simple baseline (e.g. logistic regression, majority-class predictor) before anything more complex — this is what makes a later model's improvement (or lack of it) meaningful.
- **Train/validation/test discipline:** a held-out test set is touched exactly once, at the end. No repeated peeking to "improve" test-set numbers.
- **Class imbalance:** name the imbalance ratio explicitly; document which technique was used to address it (e.g. SMOTE, class weighting) and why, per the car insurance project's precedent of transparently reporting what worked and what didn't.
- **Metric choice:** justify the primary metric against the business problem (e.g. ROC-AUC for ranking risk, precision/recall trade-off explicitly discussed for fraud detection where false negatives and false positives have different costs).
- **Honest reporting:** if a target metric isn't achievable on the available data, report the real ceiling and the reasoning — this is a hard rule, not a preference (see `docs/departments/enterprise-project-architect.md`).
- **Explainability:** any model used in a fraud/risk/compliance-adjacent context includes a SHAP (or equivalent) explanation layer — not optional given the IB/FinTech target domain.

## Examples

A results section should read like this, not like marketing copy:

> Class-weighted Random Forest achieved ROC-AUC 0.65 on the held-out test set, against an aspirational target of 0.80. The gap reflects genuine class overlap in the available features (see EDA notebook, section 3) rather than a tuning shortfall — five modeling strategies were benchmarked, and none exceeded 0.67.

## Checklist

- [ ] Baseline model established before complex models
- [ ] Test set touched only once, at the end
- [ ] Class imbalance named and technique justified
- [ ] Primary metric justified against the business problem
- [ ] Results reported honestly, including negative/ceiling results
- [ ] Explainability layer included where the domain calls for it

## References

- `docs/engineering-standards/mlops.md` — deployment/monitoring standards for models built under this standard
- `resources/glossary.md` — ROC-AUC, SHAP, SMOTE definitions

## Next Steps

- Add a model evaluation report template to `templates/` (Phase 5), structured around the honest-reporting example above.

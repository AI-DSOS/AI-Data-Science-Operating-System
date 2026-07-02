---
title: DSOS Glossary
purpose: Definitions for every domain term used more than once across the repository — checked before writing new documents to avoid duplicate or inconsistent explanations.
owner: Arulkumaran
dependencies: []
related_documents: [resources/README.md, docs/master-index.md]
version: 0.1.0
last_updated: 2026-07-02
---

## Table of Contents

- [Overview](#overview)
- [Repository Terms](#repository-terms)
- [Machine Learning Terms](#machine-learning-terms)
- [Investment Banking / FinTech Terms](#investment-banking--fintech-terms)
- [Next Steps](#next-steps)

## Overview

This is a living, alphabetized-within-category glossary. It starts with a small seed set of terms already in active use across earlier DSOS planning work (portfolio projects, bootcamp study plan) and grows as new documents are written. Abbreviation expansions are folded in here for now; split into a dedicated `abbreviation-guide.md` once this file exceeds ~30 entries.

## Repository Terms

| Term | Definition |
|---|---|
| **DSOS** | AI Data Science Operating System — this repository's short name. |
| **Module** | A self-contained unit of repo work (per `AGENTS.md`) that is fully completed, cross-linked, and logged in `CHANGELOG.md` before the next one starts. |
| **Quality Gate** | One of eight checks in `AGENTS.md` Section 7 that a document must pass before a module is marked complete. |
| **Scorecard** | `docs/progress/v1-scorecard.md` — the running count of progress against v1.0 targets. |

## Machine Learning Terms

| Term | Definition |
|---|---|
| **ROC-AUC** | Area under the Receiver Operating Characteristic curve — a threshold-independent measure of a binary classifier's ability to separate classes. |
| **SHAP** (SHapley Additive exPlanations) | A model-explainability method that attributes a prediction to each input feature's contribution, based on cooperative game theory. |
| **SMOTE** (Synthetic Minority Over-sampling Technique) | A resampling method that generates synthetic examples of a minority class to address class imbalance in training data. |
| **Isolation Forest** | An unsupervised anomaly-detection algorithm that isolates outliers by randomly partitioning the feature space; anomalies require fewer splits to isolate. |
| **LightGBM** | A gradient-boosting framework optimized for speed and memory efficiency on large tabular datasets. |
| **XGBoost** | A widely used gradient-boosting framework known for regularization support and strong performance on structured/tabular data. |

## Investment Banking / FinTech Terms

| Term | Definition |
|---|---|
| **KYC/AML** | Know Your Customer / Anti-Money Laundering — regulatory processes for verifying customer identity and detecting/reporting suspicious financial activity. |
| **Basel III** | An international regulatory framework setting bank capital adequacy, stress testing, and liquidity requirements. |
| **MiFID II** | Markets in Financial Instruments Directive II — an EU regulatory framework governing financial markets, transparency, and investor protection. |

## Next Steps

- Expand each section as new documents (engineering standards, project blueprints, prompt library) introduce terms — add the term here in the same module that first uses it.
- Split `abbreviation-guide.md` out once this file exceeds ~30 entries.
- Create `resources/reference-library.md` when the first external references (courses, papers) need to be tracked.

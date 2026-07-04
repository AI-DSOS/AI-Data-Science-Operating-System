---
title: Knowledge Map — Data Science / ML / AI Engineering Domain
purpose: The big-picture map of how the whole DS/ML/AI Engineering domain fits together, as a reference point above any single bootcamp phase's concept map.
owner: Arulkumaran
dependencies: [docs/learning-system/roadmap.md]
related_documents: [docs/learning-system/README.md, templates/concept-map-template.md]
version: 1.0.0
last_updated: 2026-07-03
---

## Table of Contents

- [Overview](#overview)
- [The Map](#the-map)
- [How to Use This](#how-to-use-this)
- [References](#references)
- [Next Steps](#next-steps)

## Overview

`templates/concept-map-template.md` produces a per-phase concept map (e.g. how this week's 3 topics relate). This document is the one level up — how the entire domain fits together, so a new concept always has a place to attach to rather than floating disconnected.

## The Map

```mermaid
graph TD
    Foundations[Python & Statistics Foundations] --> EDA[Exploratory Data Analysis]
    EDA --> Regression[Regression]
    EDA --> Classification[Classification]
    Regression --> ResidualDiag[Residual Diagnostics]
    Classification --> Imbalance[Class Imbalance: SMOTE, weighting]
    Imbalance --> Ensembles[Ensembles: RF, XGBoost, LightGBM]
    Classification --> Anomaly[Unsupervised: Isolation Forest]
    Ensembles --> Explainability[Explainability: SHAP]
    Anomaly --> Explainability

    Foundations --> DL[Deep Learning Foundations]
    DL --> NLP[NLP: tokenization, embeddings, transformers]
    NLP --> Vaagai[Applied: Vaagai Tamil Sentiment Analyzer]

    Explainability --> MLOps[MLOps: tracking, serving, monitoring]
    NLP --> MLOps
    MLOps --> Production[Production Deployment]
    Production --> InterviewReady[Interview Readiness]

    Regression -.business framing.-> IBDomain[IB/FinTech Domain: KYC/AML, Basel III, MiFID II]
    Ensembles -.business framing.-> IBDomain
    Anomaly -.business framing.-> IBDomain
    IBDomain --> InterviewReady
```

## How to Use This

When a new concept doesn't obviously connect to anything, check this map first — most genuinely new ML/DS concepts are a variant or extension of something already on here, not a disconnected island. If something truly doesn't fit, that's worth a note to the Learning Mentor about whether the map itself needs an update, not just the roadmap.

## References

- `docs/learning-system/roadmap.md` — the phase sequence this map underlies
- `templates/concept-map-template.md` — the per-phase, finer-grained version of this idea

## Next Steps

- Extend this map as Phase 4 (Deep Learning) and Phase 5 (NLP) progress and reveal which sub-branches actually matter most in practice.

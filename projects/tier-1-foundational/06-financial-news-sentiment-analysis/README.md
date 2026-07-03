---
title: Project 06 — Financial News Sentiment Analysis
purpose: NLP sentiment classification on financial news headlines, foundational NLP exercise.
owner: Arulkumaran
dependencies: [docs/engineering-standards/machine-learning.md]
related_documents: [templates/ml-pipeline-template.md]
version: 0.1.0
last_updated: 2026-07-02
---

## Status: **Blueprint only** — not started

## Business Problem
Classify financial news headlines as positive/negative/neutral sentiment, as a foundational NLP exercise relevant to market-sentiment monitoring.

## Planned Approach
Baseline TF-IDF + logistic regression, compared against a fine-tuned transformer (e.g. FinBERT-style) if time allows.

## Planned Tech Stack
Python, scikit-learn, Hugging Face Transformers.

## Target Metric
F1-score across the three sentiment classes.

## Next Steps
Source dataset, scaffold per folder-structure standard.

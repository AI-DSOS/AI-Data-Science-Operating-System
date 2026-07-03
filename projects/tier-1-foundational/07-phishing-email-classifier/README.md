---
title: Project 07 — Phishing Email Classifier
purpose: Text classification to detect phishing emails — a security-adjacent foundational NLP/classification project.
owner: Arulkumaran
dependencies: [docs/engineering-standards/machine-learning.md, docs/engineering-standards/security.md]
related_documents: [templates/ml-pipeline-template.md]
version: 0.1.0
last_updated: 2026-07-02
---

## Status: **Blueprint only** — not started

## Business Problem
Classify emails as phishing or legitimate — relevant to security operations within a bank's IT environment.

## Planned Approach
Baseline bag-of-words + logistic regression, then feature engineering on URL/sender patterns.

## Planned Tech Stack
Python, scikit-learn.

## Target Metric
Precision-weighted, since false positives (legitimate email flagged) have real workflow cost.

## Next Steps
Source dataset, scaffold per folder-structure standard.

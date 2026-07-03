---
title: Project 13 — Customer Segmentation for Wealth Management
purpose: Unsupervised clustering to segment wealth management clients for tailored service tiers.
owner: Arulkumaran
dependencies: [docs/engineering-standards/machine-learning.md]
related_documents: []
version: 0.1.0
last_updated: 2026-07-02
---

## Status: **Blueprint only** — not started

## Business Problem
Segment wealth management clients into meaningful groups (risk appetite, product affinity, engagement level) to inform advisor prioritization.

## Planned Architecture
K-means / hierarchical clustering with a feature-engineering pipeline on transaction and demographic data.

## Planned Tech Stack
Python, scikit-learn.

## Target Metric
Silhouette score plus a qualitative "does this segmentation make business sense" review — clustering has no single correct answer, so this project explicitly documents the subjective validation step.

## Next Steps
Source or simulate a client dataset.

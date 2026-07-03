---
title: Project 17 — Recommendation System for Investment Products
purpose: Recommend suitable investment products to clients based on risk profile and history.
owner: Arulkumaran
dependencies: [docs/engineering-standards/machine-learning.md]
related_documents: []
version: 0.1.0
last_updated: 2026-07-02
---

## Status: **Blueprint only** — not started

## Business Problem
Recommend investment products matched to a client's risk profile, goals, and transaction history.

## Planned Architecture
Content-based filtering on product attributes + client risk profile, with a collaborative-filtering layer if enough interaction data exists.

## Domain Context
Suitability/appropriateness assessment relevance — recommendations must be explainable against a client's stated risk tolerance, not just engagement-optimized.

## Planned Tech Stack
Python, scikit-learn, implicit (for collaborative filtering) if applicable.

## Target Metric
Precision@K on held-out recommendations, plus a suitability-consistency check (does the top recommendation match the stated risk profile).

## Next Steps
Source or simulate client + product interaction data.

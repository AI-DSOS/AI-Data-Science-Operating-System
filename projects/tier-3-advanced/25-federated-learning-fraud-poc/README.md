---
title: Project 25 — Federated Learning Proof-of-Concept for Multi-Bank Fraud Detection
purpose: The most advanced/exploratory project — a federated learning POC demonstrating awareness of privacy-preserving ML techniques relevant to multi-institution fraud collaboration.
owner: Arulkumaran
dependencies: [docs/engineering-standards/machine-learning.md]
related_documents: []
version: 0.1.0
last_updated: 2026-07-02
---

## Status: **Blueprint only** — not started; explicitly the stretch/exploratory project in the library

## Business Problem
Simulate how multiple banks could collaboratively train a fraud detection model without sharing raw transaction data — a real, discussed industry problem (banks want shared fraud signal but can't share customer data directly).

## Planned Architecture
Federated averaging simulation across 3+ synthetic "bank" data partitions, using a framework like Flower, comparing federated model performance against a centralized-data ceiling.

## Domain Context
Demonstrates awareness of privacy-preserving ML and cross-institution data-sharing constraints — a differentiated, less commonly seen portfolio piece.

## Planned Tech Stack
Python, Flower (federated learning framework), scikit-learn or PyTorch as the underlying model.

## Target Metric
Federated model performance as a percentage of the centralized-data ceiling — explicitly reported as a ceiling comparison, not an absolute number, per the honest-reporting standard.

## Next Steps
Lowest priority in the library — a stretch project for once the Aug 15 readiness deadline has passed and there's room for exploratory work.

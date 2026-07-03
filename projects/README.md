---
title: projects/ — The 25-Project Library
purpose: Index of the 25-project portfolio, tiered by difficulty, owned by the Enterprise Project Architect department.
owner: Arulkumaran
dependencies: [AGENTS.md, docs/departments/enterprise-project-architect.md, docs/engineering-standards/README.md]
related_documents: [docs/master-index.md, docs/progress/v1-scorecard.md]
version: 0.1.0
last_updated: 2026-07-02
---

## Table of Contents

- [Overview](#overview)
- [Scope of This Phase — Read This First](#scope-of-this-phase-read-this-first)
=======
- [Scope of This Phase — Read This First](#scope-of-this-phase--read-this-first)
=======
- [The Three Tiers](#the-three-tiers)
- [Status Legend](#status-legend)
- [Full Project Index](#full-project-index)
- [How a Project Graduates](#how-a-project-graduates)
- [Next Steps](#next-steps)

## Overview

25 projects, tiered by difficulty, each with a README following `templates/project-readme-template.md`. Every project is cross-referenced to the engineering standards it's built against and, where relevant, to existing work already done outside this repository.

## Scope of This Phase — Read This First

DSOS is a documentation and knowledge-management repository, not a code-execution environment with real datasets attached. **"25 production-grade projects" in this phase means 25 fully-specified blueprints** — business problem, planned architecture, tech stack, target metric, and honest current status — not 25 fully-implemented, deployed systems produced in one pass. This is the same honesty standard the repo asks every project to apply to its own results (`docs/engineering-standards/machine-learning.md`): report the real state, not an inflated one.

Three projects already have substantial real work behind them (Project 01, backfilled from a completed prior engagement; Projects 18–19, the two flagship projects with existing architecture and roadmaps; Project 22, an existing production-ready Python package; Project 21, an existing working prototype) — these are marked accordingly rather than lumped in with the 20 blueprint-only entries.

## The Three Tiers

| Tier | Focus | Projects |
|---|---|---|
| [Tier 1 — Foundational](tier-1-foundational/README.md) | Single-model fundamentals | 01–08 |
| [Tier 2 — Intermediate](tier-2-intermediate/README.md) | Full pipeline + deployment, IB/FinTech framing | 09–17 |
| [Tier 3 — Advanced](tier-3-advanced/README.md) | Full MLOps, capstones, formalized prior work | 18–25 |

## Status Legend

| Status | Meaning |
|---|---|
| Complete (backfilled) | Real work done prior to this repo; blueprint documents it here |
| Substantially built | A working package/system exists outside `projects/`, not yet migrated in |
| Prototype exists | A working proof-of-concept exists, not yet formalized |
| Scoped | Architecture and roadmap designed; implementation in progress |
| Blueprint only | Business problem and architecture planned; no implementation started |

## Full Project Index

| # | Project | Tier | Status |
|---|---|---|---|
| 01 | [Car Insurance Claim Prediction](tier-1-foundational/01-car-insurance-claim-prediction/README.md) | 1 | Complete (backfilled) |
| 02 | [Credit Card Fraud Detection](tier-1-foundational/02-credit-card-fraud-detection/README.md) | 1 | Blueprint only |
| 03 | [Loan Default Prediction](tier-1-foundational/03-loan-default-prediction/README.md) | 1 | Blueprint only |
| 04 | [Customer Churn Prediction](tier-1-foundational/04-customer-churn-prediction/README.md) | 1 | Blueprint only |
| 05 | [Stock Price Movement Classification](tier-1-foundational/05-stock-price-movement-classification/README.md) | 1 | Blueprint only |
| 06 | [Financial News Sentiment Analysis](tier-1-foundational/06-financial-news-sentiment-analysis/README.md) | 1 | Blueprint only |
| 07 | [Phishing Email Classifier](tier-1-foundational/07-phishing-email-classifier/README.md) | 1 | Blueprint only |
| 08 | [Property Price Regression](tier-1-foundational/08-property-price-regression/README.md) | 1 | Blueprint only |
| 09 | [Real-Time Transaction Fraud Detection API](tier-2-intermediate/09-realtime-transaction-fraud-api/README.md) | 2 | Blueprint only |
| 10 | [AML Transaction Monitoring & Alert Triage](tier-2-intermediate/10-aml-transaction-monitoring/README.md) | 2 | Blueprint only |
| 11 | [Credit Risk Scoring Model with Explainability](tier-2-intermediate/11-credit-risk-scoring-explainable/README.md) | 2 | Blueprint only |
| 12 | [Anomaly Detection in Trading Data](tier-2-intermediate/12-trading-data-anomaly-detection/README.md) | 2 | Blueprint only |
| 13 | [Customer Segmentation for Wealth Management](tier-2-intermediate/13-wealth-management-customer-segmentation/README.md) | 2 | Blueprint only |
| 14 | [Document Classification for KYC Onboarding](tier-2-intermediate/14-kyc-document-classification/README.md) | 2 | Blueprint only |
| 15 | [Time-Series Forecasting for Cash Flow](tier-2-intermediate/15-cashflow-time-series-forecasting/README.md) | 2 | Blueprint only |
| 16 | [NLP-Based Contract Clause Extraction](tier-2-intermediate/16-contract-clause-extraction-nlp/README.md) | 2 | Blueprint only |
| 17 | [Recommendation System for Investment Products](tier-2-intermediate/17-investment-product-recommender/README.md) | 2 | Blueprint only |
| 18 | [AI-Powered Data Quality Monitoring and Anomaly Detection Platform](tier-3-advanced/18-data-quality-monitoring-platform/README.md) | 3 | Scoped (flagship) |
| 19 | [Intelligent Defect Classification and Root Cause Prediction](tier-3-advanced/19-defect-classification-root-cause/README.md) | 3 | Scoped (flagship) |
| 20 | [End-to-End MLOps Fraud Detection Platform](tier-3-advanced/20-mlops-fraud-detection-platform/README.md) | 3 | Blueprint only |
| 21 | [Multi-Agent QA Automation Orchestrator](tier-3-advanced/21-multi-agent-qa-orchestrator/README.md) | 3 | Prototype exists |
| 22 | [Regulatory Reporting Automation](tier-3-advanced/22-regulatory-reporting-automation/README.md) | 3 | Substantially built |
| 23 | [Conversational AI Risk Assistant](tier-3-advanced/23-conversational-risk-assistant/README.md) | 3 | Blueprint only |
| 24 | [Real-Time Market Risk Dashboard with Streaming Data](tier-3-advanced/24-realtime-market-risk-dashboard/README.md) | 3 | Blueprint only |
| 25 | [Federated Learning Proof-of-Concept for Multi-Bank Fraud Detection](tier-3-advanced/25-federated-learning-fraud-poc/README.md) | 3 | Blueprint only |

## How a Project Graduates

Blueprint → Scoped (architecture detailed, ADRs started) → Implemented (real `src/`, `tests/`, following `docs/engineering-standards/folder-structure.md`) → Production-grade (passes `templates/production-checklist-template.md` in full). A project's status here should always reflect its real, current state — updating it dishonestly defeats the purpose of tracking it at all.

## Next Steps

- Prioritize which blueprint-only projects get implemented first — likely Projects 02 and 03 (they're dependencies for Tier 2/3 projects 09, 11, 20).
- Migrate the `nhecf` package (Project 22) and the multi-agent QA POC (Project 21) into this structure, since both already exist substantially.
- Update `trackers/project-tracker.md` with real entries for all 25 once implementation begins.

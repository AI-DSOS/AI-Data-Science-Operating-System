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
| 01 | Car Insurance Claim Prediction | 1 | Complete (backfilled) |
| 02 | Credit Card Fraud Detection | 1 | Blueprint only |
| 03 | Loan Default Prediction | 1 | Blueprint only |
| 04 | Customer Churn Prediction | 1 | Blueprint only |
| 05 | Stock Price Movement Classification | 1 | Blueprint only |
| 06 | Financial News Sentiment Analysis | 1 | Blueprint only |
| 07 | Phishing Email Classifier | 1 | Blueprint only |
| 08 | Property Price Regression | 1 | Blueprint only |
| 09 | Real-Time Transaction Fraud Detection API | 2 | Blueprint only |
| 10 | AML Transaction Monitoring & Alert Triage | 2 | Blueprint only |
| 11 | Credit Risk Scoring Model with Explainability | 2 | Blueprint only |
| 12 | Anomaly Detection in Trading Data | 2 | Blueprint only |
| 13 | Customer Segmentation for Wealth Management | 2 | Blueprint only |
| 14 | Document Classification for KYC Onboarding | 2 | Blueprint only |
| 15 | Time-Series Forecasting for Cash Flow | 2 | Blueprint only |
| 16 | NLP-Based Contract Clause Extraction | 2 | Blueprint only |
| 17 | Recommendation System for Investment Products | 2 | Blueprint only |
| 18 | AI-Powered Data Quality Monitoring and Anomaly Detection Platform | 3 | Scoped (flagship) |
| 19 | Intelligent Defect Classification and Root Cause Prediction | 3 | Scoped (flagship) |
| 20 | End-to-End MLOps Fraud Detection Platform | 3 | Blueprint only |
| 21 | Multi-Agent QA Automation Orchestrator | 3 | Prototype exists |
| 22 | Regulatory Reporting Automation | 3 | Substantially built |
| 23 | Conversational AI Risk Assistant | 3 | Blueprint only |
| 24 | Real-Time Market Risk Dashboard with Streaming Data | 3 | Blueprint only |
| 25 | Federated Learning Proof-of-Concept for Multi-Bank Fraud Detection | 3 | Blueprint only |

## How a Project Graduates

Blueprint → Scoped (architecture detailed, ADRs started) → Implemented (real `src/`, `tests/`, following `docs/engineering-standards/folder-structure.md`) → Production-grade (passes `templates/production-checklist-template.md` in full). A project's status here should always reflect its real, current state — updating it dishonestly defeats the purpose of tracking it at all.

## Next Steps

- Prioritize which blueprint-only projects get implemented first — likely Projects 02 and 03 (they're dependencies for Tier 2/3 projects 09, 11, 20).
- Migrate the `nhecf` package (Project 22) and the multi-agent QA POC (Project 21) into this structure, since both already exist substantially.
- Update `trackers/project-tracker.md` with real entries for all 25 once implementation begins.

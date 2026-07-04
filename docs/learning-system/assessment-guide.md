---
title: Assessment Guide — How Learning Connects to Formal Assessment
purpose: How completed learning (per the roadmap and mastery rubrics) hands off to formal assessment by the Technical Interviewer department.
owner: Arulkumaran
dependencies: [docs/departments/technical-interviewer.md]
related_documents: [docs/learning-system/README.md, docs/learning-system/mastery-rubric-methodology.md]
version: 1.0.0
last_updated: 2026-07-03
---

## Table of Contents

- [Overview](#overview)
- [The Handoff Rule](#the-handoff-rule)
- [Assessment Cadence by Phase](#assessment-cadence-by-phase)
- [References](#references)

## Overview

Learning and assessment are deliberately separate departments (Learning Mentor teaches; Technical Interviewer assesses) — this document is the explicit handoff point between them, so a concept doesn't sit "learned" indefinitely without ever being tested under interview-like pressure.

## The Handoff Rule

A concept reaching Mastery Level 3 ("Applies") per `docs/learning-system/mastery-rubric-methodology.md` becomes eligible for inclusion in the next mock interview session — it doesn't wait for Level 5. Testing a concept under pressure at Level 3 is itself a valid part of solidifying it further, not just a checkpoint after mastery is "finished."

## Assessment Cadence by Phase

| Phase | Assessment Focus |
|---|---|
| 1–2 (Complete) | Foundational theory + the two completed regression sprint sessions' concepts |
| 3 (In Progress) | Imbalanced-data techniques, ensemble methods, explainability — tested via `prompts/mock-interviews/shap-smote-drilldown.md` |
| 4 | Deep learning fundamentals, lighter assessment weight (breadth over depth expected) |
| 5 | NLP fundamentals + the Vaagai capstone as a real project-walkthrough assessment subject |
| 6 | Full-loop simulations only (`prompts/mock-interviews/full-loop-simulation.md`) — no new-topic assessment, per the roadmap's Interview Readiness Checkpoint |

## References

- `docs/departments/technical-interviewer.md`
- `docs/learning-system/roadmap.md`, `mastery-rubric-methodology.md`

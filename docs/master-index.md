---
title: DSOS Master Index
purpose: Single flat list of every document in the repository, one line each — the first place to check before writing anything new, to avoid duplicate content.
owner: Arulkumaran
dependencies: []
related_documents: [AGENTS.md, docs/progress/v1-scorecard.md, docs/document-map.md]
version: 0.1.0
last_updated: 2026-07-02
---

## Table of Contents

- [Overview](#overview)
- [Root](#root)
- [docs/](#docs)
- [prompts/](#prompts)
- [templates/](#templates)
- [trackers/](#trackers)
- [playbooks/](#playbooks)
- [projects/](#projects)
- [resources/](#resources)
- [journal/](#journal)
- [assets/](#assets)
- [.github/](#github)
- [How to Use This Index](#how-to-use-this-index)
- [Next Steps](#next-steps)

## Overview

Every Markdown file in the repository must have a line here. This is a flat list (not a hierarchy diagram — that's `docs/document-map.md`). Update this file in the same change that adds, moves, or removes any document.

## Root

| File | Purpose |
|---|---|
| `AGENTS.md` | Governance rules for AI agents working in this repo |
| `README.md` | Human-facing entry point |
| `mkdocs.yml` | Documentation site configuration (not a Markdown doc, tracked for completeness) |

## docs/

| File | Purpose |
|---|---|
| `docs/README.md` | Index and purpose of the `docs/` folder |
| `docs/master-index.md` | This file |
| `docs/document-map.md` | Mermaid relationship graph of documents |
| `docs/CHANGELOG.md` | Dated log of module-by-module changes |
| `docs/progress/README.md` | Index and purpose of the `docs/progress/` folder |
| `docs/progress/v1-scorecard.md` | Running progress count against v1.0 targets |
| `docs/departments/README.md` | Index and shared context for the 5 departments |
| `docs/departments/learning-mentor.md` | Department spec — teaching, roadmaps, bootcamp tracking |
| `docs/departments/enterprise-project-architect.md` | Department spec — the 25-project portfolio, architecture |
| `docs/departments/technical-interviewer.md` | Department spec — mock interviews, readiness scoring |
| `docs/departments/career-brand-coach.md` | Department spec — resume, LinkedIn, GitHub, recruiter tracking |
| `docs/departments/cto.md` | Department spec — governance, prioritization, quality gates |
| `docs/operating-system/README.md` | Index and cadence map for the 11 operating-system documents |
| `docs/operating-system/daily-operating-system.md` | Weekday/Sunday time structure and daily logging |
| `docs/operating-system/weekly-review.md` | Weekly CTO-run checkpoint across all departments |
| `docs/operating-system/monthly-board-meeting.md` | Monthly formal reporting + scorecard reconciliation |
| `docs/operating-system/quarterly-review.md` | Quarterly wide-lens roadmap and trajectory check |
| `docs/operating-system/annual-review.md` | Annual full-system and career-outcome review |
| `docs/operating-system/sprint-planning.md` | How modules/phases/project milestones get scoped before starting |
| `docs/operating-system/knowledge-management.md` | Process rules for keeping index/map/glossary/changelog accurate |
| `docs/operating-system/task-prioritization.md` | Default priority order across bootcamp, projects, career, Vaagai |
| `docs/operating-system/time-blocking.md` | Default weekly time-block map |
| `docs/operating-system/deep-work.md` | What qualifies as protected deep-focus time and why |
| `docs/operating-system/revision-strategy.md` | How mastered concepts get revisited so they don't decay |
| `docs/operating-system/reflection-system.md` | Lightweight sustainability/fit checks on the system itself |
| `docs/career-system/README.md` | Index and layer distinction for the 7 career strategy docs |
| `docs/career-system/resume-framework.md` | Positioning strategy, version strategy per target role type |
| `docs/career-system/linkedin-strategy.md` | Content pillars, cadence, voice |
| `docs/career-system/github-strategy.md` | Pinned repos strategy, README standard |
| `docs/career-system/portfolio-strategy.md` | Cross-channel consistency, anchor projects |
| `docs/career-system/networking-plan.md` | Target contacts, outreach principles, Chennai/IB context |
| `docs/career-system/conference-preparation.md` | Event selection, preparation discipline |
| `docs/career-system/technical-writing-guide.md` | Article selection, structure, honest-results emphasis |
| `docs/engineering-standards/README.md` | Index of the 15 engineering standards documents |
| `docs/engineering-standards/python.md` | Python style, typing, dependency management |
| `docs/engineering-standards/sql.md` | SQL formatting, naming, migrations |
| `docs/engineering-standards/jupyter.md` | Notebook location, naming, graduation to `src/` |
| `docs/engineering-standards/fastapi.md` | API structure, validation, versioning, health checks |
| `docs/engineering-standards/docker.md` | Base images, multi-stage builds, non-root, `.dockerignore` |
| `docs/engineering-standards/machine-learning.md` | Baselines, train/test discipline, honest metric reporting |
| `docs/engineering-standards/mlops.md` | Tracking, registry, serving, monitoring, drift, retraining |
| `docs/engineering-standards/git-github-workflow.md` | Branch strategy, commit messages, code review, GitHub conventions |
| `docs/engineering-standards/testing.md` | Unit, data, model, and integration testing |
| `docs/engineering-standards/logging.md` | Structured logging, levels, correlation IDs, no secrets |
| `docs/engineering-standards/documentation.md` | Code-level docs — docstrings, project READMEs, ADRs |
| `docs/engineering-standards/naming-conventions.md` | Code-level naming — Python, SQL, model artifacts, env vars |
| `docs/engineering-standards/folder-structure.md` | Standard project-level folder layout |
| `docs/engineering-standards/security.md` | Secrets, input validation, least privilege, PII handling |
| `docs/engineering-standards/performance-and-scalability.md` | Baselines, latency targets, stateless design, batch vs. real-time |
=======

## prompts/

**104 prompts across 12 categories, indexed in full in [`prompts/README.md`](../prompts/README.md).** Learning (10), Projects (10), Code Reviews (8), Architecture Reviews (8), Mock Interviews (10), Debugging (8), System Design (8), Technical Writing (8), Career Planning (10), Research (8), Documentation (8), Repository Maintenance (8).

## templates/

**50 templates, indexed in full in [`templates/README.md`](../templates/README.md).** Grouped: Project Blueprint (15), Learning System (5), Interview/Assessment (4), Career System (8), Operating System/Review (5), Engineering/Code (8), Governance (5).

## trackers/

**14 trackers, indexed in full in [`trackers/README.md`](../trackers/README.md).** Daily, weekly, monthly, learning, coding, project, git, GitHub, reading, portfolio, interview, confidence, habit, KPI dashboard.

## playbooks/

*Not started. Target categories: learning a new topic, starting a new project, debugging production issues, preparing for interviews, publishing a GitHub repository, writing technical articles, building a portfolio, sprint planning, weekly review, monthly board meeting.*

## projects/

**25 projects across 3 tiers, indexed in full in [`projects/README.md`](../projects/README.md).** Tier 1 — Foundational (01–08), Tier 2 — Intermediate (09–17), Tier 3 — Advanced (18–25). See that index for the important scope note: these are 25 fully-specified blueprints, not 25 fully-implemented systems — 3 projects have substantial prior work behind them (backfilled/prototype/substantially-built), the rest are blueprint-only pending implementation.

## resources/

| File | Purpose |
|---|---|
| `resources/README.md` | Index and purpose of the `resources/` folder |
| `resources/glossary.md` | Domain term definitions (repo, ML, IB/FinTech terms) |

*Remaining target: abbreviation guide (folded into glossary for now), reference library.*

## journal/

*Not started.*

## assets/

*Not started.*

## .github/

| File | Purpose |
|---|---|
| `.github/README.md` | Index and purpose of the `.github/` folder |
| `.github/workflows/deploy-docs.yml` | CI workflow — builds and deploys the MkDocs site on push to `main` |

*Remaining target: issue templates, PR template.*

## How to Use This Index

- **Before writing a new document:** search this file (Ctrl+F the topic) to check nothing equivalent already exists.
- **After creating a document:** add one row to the relevant section, in the same change.
- **After deleting or moving a document:** remove or update its row in the same change.

## Next Steps

- Populate `docs/document-map.md` once more than ~10 documents exist (a 5-node graph isn't worth diagramming yet).
- Convert the "not started" category placeholders into real tables as each folder gets its first files (Phase 5 onward per `AGENTS.md` Section 10).

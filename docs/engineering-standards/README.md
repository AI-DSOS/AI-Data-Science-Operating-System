---
title: docs/engineering-standards/ — Engineering Standards
purpose: Index of the engineering standards that govern every project in projects/ and every code snippet referenced elsewhere in DSOS. Enforced primarily by the Enterprise Project Architect department.
owner: Arulkumaran
dependencies: [AGENTS.md, docs/departments/enterprise-project-architect.md]
related_documents: [docs/master-index.md, docs/departments/enterprise-project-architect.md]
version: 0.1.0
last_updated: 2026-07-02
---

## Table of Contents

- [Overview](#overview)
- [Standards in This Module](#standards-in-this-module)
- [How Standards Get Enforced](#how-standards-get-enforced)
- [Precedence](#precedence)
- [Next Steps](#next-steps)

## Overview

The original DSOS master prompt calls for standards across 19 named areas (Python, Git, GitHub, SQL, Jupyter, FastAPI, Docker, ML, MLOps, Logging, Testing, Documentation, Naming Conventions, Folder Structure, Code Review, Branch Strategy, Commit Messages, Security, Performance, Scalability). To avoid 19 thin, overlapping documents, closely related areas are grouped into 15 standards documents below — each still names every original area it covers.

## Standards in This Module

| Document | Covers |
|---|---|
| [`python.md`](python.md) | Python |
| [`sql.md`](sql.md) | SQL |
| [`jupyter.md`](jupyter.md) | Jupyter |
| [`fastapi.md`](fastapi.md) | FastAPI |
| [`docker.md`](docker.md) | Docker |
| [`machine-learning.md`](machine-learning.md) | Machine Learning |
| [`mlops.md`](mlops.md) | MLOps |
| [`git-github-workflow.md`](git-github-workflow.md) | Git, GitHub, Branch Strategy, Commit Messages, Code Review |
| [`testing.md`](testing.md) | Testing |
| [`logging.md`](logging.md) | Logging |
| [`documentation.md`](documentation.md) | Documentation (code-level; repo-level docs standard lives in `AGENTS.md` Section 6) |
| [`naming-conventions.md`](naming-conventions.md) | Naming Conventions (code-level; repo-file naming lives in `AGENTS.md` Section 8) |
| [`folder-structure.md`](folder-structure.md) | Folder Structure (project-level; repo-level structure lives in `AGENTS.md` Section 3) |
| [`security.md`](security.md) | Security |
| [`performance-and-scalability.md`](performance-and-scalability.md) | Performance, Scalability |

## How Standards Get Enforced

The Enterprise Project Architect department applies these standards to every project in `projects/` (Phase 7) and checks them in its Weekly Workflow (per `docs/departments/enterprise-project-architect.md`). A project is not "done" if it violates a standard here without a documented, reasoned exception.

## Precedence

Where a repo-level rule in `AGENTS.md` and a code-level rule here appear to overlap (e.g. naming, documentation, folder structure), `AGENTS.md` governs the repository's own Markdown files and structure; the documents in this folder govern the code and artifacts *inside* project folders.

## Next Steps

- Reference these standards from each project blueprint as `projects/` is built out (Phase 7).
- Revisit whether any of the 15 documents need splitting once real project work surfaces gaps (raise at Quarterly Review).

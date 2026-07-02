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

## prompts/

*Not started. Target: 100+ files across learning, projects, code review, architecture review, mock interviews, debugging, system design, technical writing, career planning, research, documentation, repository maintenance.*

## templates/

*Not started. Target: 50 files across trackers, project templates, review templates, career templates, prompt templates.*

## trackers/

*Not started. Target categories: daily, weekly, monthly, learning, coding, project, git, GitHub, reading, portfolio, interview, confidence, habit, KPI dashboard.*

## playbooks/

*Not started. Target categories: learning a new topic, starting a new project, debugging production issues, preparing for interviews, publishing a GitHub repository, writing technical articles, building a portfolio, sprint planning, weekly review, monthly board meeting.*

## projects/

*Not started. Target: 25 production-grade projects, tiered by difficulty.*

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

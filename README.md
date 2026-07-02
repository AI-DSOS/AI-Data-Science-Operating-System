---
title: AI Data Science Operating System (DSOS)
purpose: Human-facing entry point to the repository — what DSOS is, how it's organized, and where to start.
owner: Arulkumaran
dependencies: [AGENTS.md]
related_documents: [AGENTS.md, docs/master-index.md, docs/progress/v1-scorecard.md]
version: 0.1.0
last_updated: 2026-07-02
---

# AI Data Science Operating System (DSOS)

DSOS is a single source of truth for a complete Data Science / ML / AI Engineering career transformation — learning system, project portfolio, engineering standards, career system, and the governance layer that keeps all of it consistent as it grows.

It is built and maintained with the help of AI agents operating under the rules in [`AGENTS.md`](AGENTS.md). If you are an AI agent reading this repository for the first time, read `AGENTS.md` before making any change.

## What's Here

| Folder | What it contains |
|---|---|
| [`docs/`](docs/README.md) | Departments, operating system, engineering standards, learning system, career system, knowledge management |
| `prompts/` | Reusable prompt library (target: 100+ files) |
| `templates/` | Reusable Markdown templates (target: 50) |
| `trackers/` | Daily/weekly/monthly/KPI trackers |
| `playbooks/` | Step-by-step operational playbooks |
| `projects/` | 25 production-grade project blueprints, tiered by difficulty |
| `resources/` | Glossary, abbreviation guide, reference library |
| `journal/` | Learning and reflection journal |
| `assets/` | Diagrams and exported artifacts |
| `.github/` | Issue/PR templates and CI workflows, including the docs-site deploy |

## v1.0 Target

- ~100 Markdown documents
- 25 production-grade projects
- 50 reusable templates
- 100+ prompt files
- A documentation site generated from this Markdown (MkDocs)

Live progress against these numbers is tracked in [`docs/progress/v1-scorecard.md`](docs/progress/v1-scorecard.md).

## Where to Start

- **New here?** Start with [`docs/master-index.md`](docs/master-index.md) — a flat list of every document in the repo.
- **Contributing (human or agent)?** Read [`AGENTS.md`](AGENTS.md) first — it defines the documentation standard, naming conventions, quality gates, and the module-by-module build discipline this repo follows.
- **Want the roadmap?** See `AGENTS.md` Section 10 for the phase-by-phase build order toward v1.0.

## Status

DSOS is in **Phase 1: Foundation**. See [`docs/progress/v1-scorecard.md`](docs/progress/v1-scorecard.md) for current counts and [`docs/CHANGELOG.md`](docs/CHANGELOG.md) for what's changed, module by module.

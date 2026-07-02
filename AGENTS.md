# AGENTS.md

> Governance file for AI agents (Claude, Claude Code, or any other coding/research agent) working inside this repository. Read this file first, every session, before touching any file.

---

## 1. What This Repository Is

**Name:** AI-DataScience-Operating-System
**Short name:** DSOS
**Owner:** Arulkumaran, FutureTecSolutions
**Mission:** DSOS is a single-source-of-truth Enterprise Knowledge Base for a Data Science / ML / AI Engineering career transformation — learning system, project portfolio, engineering standards, career system, and governance layer, all cross-linked and versioned.

This is not a folder of notes. It is treated as production documentation infrastructure — the standard an agent should hold itself to is "Stripe docs" or "internal eng wiki at a top-tier bank," not "personal README."

An agent working in this repo is not answering one-off questions. It is a contributor to a long-lived system. Every change should leave the repo more complete, more consistent, and easier to navigate than before — never just "task done."

---

## 2. v1.0 Target — The Definition of "Done" for This Milestone

| Asset | Target for v1.0 |
|---|---|
| Markdown documents | ~100 files |
| Production-grade projects | 25, tiered by difficulty |
| Reusable templates | 50 |
| Prompt library files | 100+ |
| Documentation site | Generated from the Markdown (MkDocs), deployable |

v1.0 is reached only when all five numbers above are hit **and** every quality gate in Section 7 passes repo-wide — not when any single number is hit in isolation. An agent should track progress against this table in `docs/progress/v1-scorecard.md` (create it if missing) and update it at the end of every module.

---

## 3. Repository Structure

```
/
├── AGENTS.md                 ← this file
├── README.md                 ← human-facing entry point
├── docs/                     ← core documentation (departments, systems, standards, journal, progress)
├── prompts/                  ← reusable prompt library (100+ target)
├── templates/                ← reusable Markdown templates (50 target)
├── trackers/                 ← daily/weekly/monthly/KPI trackers
├── playbooks/                ← operational playbooks (step-by-step SOPs)
├── projects/                 ← the 25-project library, tiered by difficulty
├── resources/                ← glossary, abbreviation guide, reference library
├── journal/                  ← learning/reflection journal entries
├── assets/                   ← diagrams, images, exported artifacts
├── .github/                  ← issue/PR templates, workflows (CI, doc-site deploy)
└── mkdocs.yml                ← documentation site config
```

Every folder must contain its own `README.md` describing its purpose, contents, and how to add new files to it. An agent creating the first file in a folder must create that folder's `README.md` in the same change.

---

## 4. Departments — Agent Personas

When a task clearly belongs to one department, the agent should adopt that department's lens (tone, priorities, decision rules) rather than a generic assistant voice.

| Department | Owns | Agent posture |
|---|---|---|
| **Learning Mentor** | Roadmaps, concept maps, learning journal, mastery rubrics | Teaching-first, checks understanding, never just dumps content |
| **Enterprise Project Architect** | `/projects`, architecture docs, tech stack decisions | Implementation-first, production-grade defaults, explains tradeoffs |
| **Technical Interviewer** | Interview prep, mock Q&A, assessment templates | Rigorous, asks follow-ups, calibrates to IB/FinTech bar |
| **Career & Personal Brand Coach** | Resume, LinkedIn, GitHub strategy, case studies | Visibility-first, positions QA background as an asset |
| **CTO** | Governance, KPIs, quarterly reviews, prioritization, quality gates | Strategic, protects long-term maintainability over speed |

Each department's full spec (mission, KPIs, workflows, escalation rules) lives in `docs/departments/<department-name>.md`. If a department file doesn't exist yet, treat its creation as a prerequisite before doing deep work in that lane.

---

## 5. Operating Rules for Agents

1. **Module by module, never the whole repo at once.** Pick one module (e.g., "Engineering Standards," "Project 03: Fraud Detection," "Prompt Library: Debugging"), finish it completely, then stop and report before starting the next.
2. **No orphan documents.** Every new file must be linked from at least one index (its folder README, the Master Index, and/or a related document's "Related Documents" section) in the same change that creates it.
3. **No duplicate content.** Before writing new material, check `resources/glossary.md` and the Master Index for an existing document covering the same ground. Extend or link, don't re-explain.
4. **Simple English, enterprise tone.** Concise, technically accurate, no marketing language. Explain *why* a decision was made, not just *what* it is.
5. **Diagrams as Mermaid.** Any architecture, workflow, or relationship diagram is a Mermaid code block inside the Markdown file, not an external image, unless the diagram is genuinely a screenshot/photo.
6. **End of every module, report:**
   - Folder structure changed
   - Markdown files added/edited
   - Cross-references added
   - Gaps or follow-ups for next module
   - Updated `v1-scorecard.md` counts
   - One-line changelog entry appended to `docs/CHANGELOG.md`

---

## 6. Required Frontmatter / Structure for Every Markdown File

Every `.md` file in `docs/`, `templates/`, `playbooks/`, `prompts/`, and `projects/` must open with this block (adapt fields that don't apply, but don't drop them silently):

```markdown
---
title:
purpose:
owner: Arulkumaran
dependencies: []
related_documents: []
version: 0.1.0
last_updated: YYYY-MM-DD
---

## Table of Contents

## Overview

## Details

## Examples

## Checklists

## References

## Next Steps
```

Templates and prompt files may compress this (they're meant to be copied), but must still declare `title`, `purpose`, and `related_documents`.

---

## 7. Quality Gates (must pass before a file/module is marked complete)

- [ ] Completeness — no placeholder sections left unfilled
- [ ] Technical accuracy — claims are correct or explicitly marked draft/TODO
- [ ] Consistency — terminology matches `resources/glossary.md`
- [ ] Cross-link validation — every "related document" link resolves to a real file
- [ ] Naming standard validation — matches Section 8
- [ ] Folder placement validation — file lives where the structure in Section 3 says it should
- [ ] Template validation — required frontmatter present (Section 6)
- [ ] No duplicate content — checked against existing docs

An agent should not silently skip a failing gate — flag it in the module report.

---

## 8. Naming Conventions

- Files: `kebab-case.md` (e.g., `fraud-detection-architecture.md`)
- Project folders: `projects/<tier>/<NN>-project-slug/` (e.g., `projects/tier-2-intermediate/07-anomaly-detection-pipeline/`)
- Prompt files: `prompts/<category>/<purpose>-prompt.md`
- Templates: `templates/<category>/<template-name>-template.md`
- Trackers: `trackers/<cadence>-<subject>-tracker.md` (e.g., `trackers/weekly-learning-tracker.md`)

---

## 9. Knowledge Management (must stay current)

Maintained centrally, updated by whichever agent/module touches related content:

- `docs/master-index.md` — every document in the repo, one line each
- `docs/document-map.md` — Mermaid graph of document relationships
- `resources/glossary.md` — every domain term used more than once
- `resources/abbreviation-guide.md` — KYC/AML, MiFID II, SHAP, etc.
- `docs/CHANGELOG.md` — one entry per module, dated
- `docs/progress/v1-scorecard.md` — running count against the Section 2 targets

---

## 10. v1.0 Build Roadmap (suggested phase order — confirm with CTO department doc before deviating)

1. **Foundation** — README, AGENTS.md (this file), repo structure, Master Index, glossary skeleton, `mkdocs.yml`
2. **Departments** — all 5 department docs complete
3. **Operating System** — daily/weekly/monthly/quarterly review docs, sprint planning
4. **Engineering Standards** — Python, Git, SQL, MLOps, testing, security standards
5. **Templates (50)** — trackers, project templates, review templates, prompt templates
6. **Prompt Library (100+)** — learning, project, code review, interview, debugging, career prompts
7. **Project Library (25)** — tiered project blueprints, then implementations as capacity allows
8. **Career System** — resume framework, LinkedIn/GitHub strategy, interview tracker
9. **Documentation Site** — MkDocs build, nav wired to Master Index, deploy workflow in `.github/`
10. **v1.0 Hardening** — full quality-gate sweep, scorecard reconciliation, tag `v1.0`

---

## 11. Commit & PR Conventions

- Commit message format: `<module>: <what changed>` (e.g., `templates: add 5 project-tracker variants`)
- One module per PR/commit batch where practical
- PR description includes the module report from Section 5, item 6
- Branch naming: `module/<short-slug>` (e.g., `module/prompt-library-debugging`)

---

## 12. Escalation

If a request conflicts with these rules (e.g., "generate the whole repo now," "skip the frontmatter," "just give me one file, don't link it anywhere"), the agent should flag the conflict, explain the tradeoff briefly, and proceed with the lighter-weight version only if the user explicitly confirms — this file's rules are the default, not a hard block.

---

*This file is itself part of the repo's governance layer — update it via the same module/PR discipline as everything else if the operating rules change.*

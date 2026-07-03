---
title: docs/ — Core Documentation
purpose: Entry point and index for all core documentation — departments, operating system, engineering standards, learning system, career system, progress tracking, and knowledge management artifacts.
owner: Arulkumaran
dependencies: [AGENTS.md]
related_documents: [docs/master-index.md, docs/progress/v1-scorecard.md]
version: 0.1.0
last_updated: 2026-07-02
---

## Table of Contents

- [Overview](#overview)
- [Subfolders](#subfolders)
- [How to Add a Document Here](#how-to-add-a-document-here)
- [Next Steps](#next-steps)

## Overview

`docs/` holds every core knowledge document that isn't a template, prompt, tracker, playbook, or project — i.e. the "read this to understand how DSOS works" layer of the repository. This includes department specs, the operating system (daily/weekly/monthly/quarterly rhythms), engineering standards, the learning system, the career system, and the knowledge-management artifacts that keep the whole repo navigable.

**This file also serves as the MkDocs site homepage** (`docs_dir` is `docs/`, and MkDocs treats a folder's `README.md` as its index page automatically). See [`documentation-site.md`](documentation-site.md) for why the site is scoped to `docs/` only.

### On GitHub Only (Not Part of This Site)

| Item | Where |
|---|---|
| `AGENTS.md` — governance rules for AI agents working in this repo | [View on GitHub](https://github.com/AI-DSOS/AI-Data-Science-Operating-System/blob/main/AGENTS.md) |
| `templates/` — 50 reusable templates | [View on GitHub](https://github.com/AI-DSOS/AI-Data-Science-Operating-System/tree/main/templates) |
| `trackers/` — 14 reusable trackers | [View on GitHub](https://github.com/AI-DSOS/AI-Data-Science-Operating-System/tree/main/trackers) |
| `prompts/` — 104 reusable prompts | [View on GitHub](https://github.com/AI-DSOS/AI-Data-Science-Operating-System/tree/main/prompts) |
| `projects/` — the 25-project library | [View on GitHub](https://github.com/AI-DSOS/AI-Data-Science-Operating-System/tree/main/projects) |
| `resources/` — glossary and reference material | [View on GitHub](https://github.com/AI-DSOS/AI-Data-Science-Operating-System/tree/main/resources) |

## Subfolders

| Folder | Contents | Status |
|---|---|---|
| `departments/` | The 5 department specs (Learning Mentor, Enterprise Project Architect, Technical Interviewer, Career & Personal Brand Coach, CTO) | Not yet created |
| `operating-system/` | Daily/weekly/monthly/quarterly/annual review docs, sprint planning | Not yet created |
| `learning-system/` | Roadmaps, concept maps, mastery rubrics | Not yet created |
| `engineering-standards/` | Python, Git, SQL, MLOps, testing, security standards | Not yet created |
| `career-system/` | Resume framework, LinkedIn/GitHub strategy | Not yet created |
| `progress/` | v1.0 scorecard and phase-tracking docs | **Created — see `progress/README.md`** |

Root-level files directly in `docs/` (not in a subfolder) are cross-cutting knowledge-management artifacts: `master-index.md`, `document-map.md`, `CHANGELOG.md`.

## How to Add a Document Here

1. Confirm the document doesn't already exist (`master-index.md`).
2. Place it in the correct subfolder per the table above; create the subfolder + its `README.md` if this is the first file in it.
3. Use the frontmatter template from `AGENTS.md` Section 6.
4. Add a line for it to `docs/master-index.md`.
5. Link it from at least one related document's `related_documents` field.

## Next Steps

- Create `departments/`, `operating-system/`, `learning-system/`, `engineering-standards/`, `career-system/` as their content is drafted (see AGENTS.md Section 10 build roadmap, Phase 2 onward). None of these subfolders exist yet — Phase 2 starts with `departments/`.

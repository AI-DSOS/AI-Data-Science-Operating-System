---
title: prompts/ — Reusable Prompt Library
purpose: Index of the 104 reusable prompts across 12 categories, meeting the v1.0 "100+ prompt files" target.
owner: Arulkumaran
dependencies: [AGENTS.md]
related_documents: [docs/master-index.md, templates/README.md]
version: 0.1.0
last_updated: 2026-07-02
---

## Table of Contents

- [Overview](#overview)
- [The 12 Categories](#the-12-categories)
- [How Prompts Differ from Templates](#how-prompts-differ-from-templates)
- [How to Use a Prompt](#how-to-use-a-prompt)
- [Next Steps](#next-steps)

## Overview

Each prompt file is a single copy-paste-ready prompt with `{variables}` to fill in, plus a one-line "Use When" note pointing to the department or operating-system document that calls for it. Prompts are intentionally short — the value is in having 104 pre-built starting points, not in each one being a long document.

## The 12 Categories

| Category | Count | Folder |
|---|---|---|
| Learning | 10 | `learning/` |
| Projects | 10 | `projects/` |
| Code Reviews | 8 | `code-reviews/` |
| Architecture Reviews | 8 | `architecture-reviews/` |
| Mock Interviews | 10 | `mock-interviews/` |
| Debugging | 8 | `debugging/` |
| System Design | 8 | `system-design/` |
| Technical Writing | 8 | `technical-writing/` |
| Career Planning | 10 | `career-planning/` |
| Research | 8 | `research/` |
| Documentation | 8 | `documentation/` |
| Repository Maintenance | 8 | `repository-maintenance/` |
| **Total** | **104** | |

## How Prompts Differ from Templates

`templates/` (Phase 5) holds document *shapes* to fill in — a project README, an ADR, a tracker. `prompts/` holds *instructions* to give an AI agent (or use as a personal thinking prompt) that often produce content *for* those templates. A prompt like `technical-writing/case-study-drafting.md` exists to fill in `templates/case-study-template.md`.

## How to Use a Prompt

Copy the text inside the ` ``` ` block, replace `{variables}` with real specifics, and use it directly in a conversation or paste it as a task instruction. The "Use When" line tells you which department workflow or operating-system moment it's built for.

## Next Steps

- Track which prompts get used most, and retire or rewrite ones that don't hold up in practice — revisit at the first Quarterly Review.
- Add prompts for any gap that surfaces once Phase 7 (Project Library) is underway and real usage patterns emerge.

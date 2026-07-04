---
title: docs/learning-system/ — Learning System
purpose: The actual curriculum content layer — roadmap, knowledge map, revision plan, and progress-tracking methodology — distinct from the Learning Mentor department (who owns it), operating-system docs (when it happens), and templates (fill-in artifacts).
owner: Arulkumaran
dependencies: [AGENTS.md, docs/departments/learning-mentor.md]
related_documents: [docs/master-index.md, docs/departments/learning-mentor.md]
version: 1.0.0
last_updated: 2026-07-03
---

## Table of Contents

- [Overview](#overview)
- [How This Differs from Related Folders](#how-this-differs-from-related-folders)
- [The Documents](#the-documents)
- [Next Steps](#next-steps)

## Overview

Named in the original DSOS master prompt as its own "LEARNING SYSTEM" section, distinct from the Learning Mentor department spec — this folder was referenced by `docs/departments/learning-mentor.md` from Phase 2 onward but never actually built until this v1.1 module.

## How This Differs from Related Folders

| Layer | Answers | Example |
|---|---|---|
| `docs/departments/learning-mentor.md` | Who's responsible, KPIs, workflows | "Learning Mentor teaches; owns the journal" |
| `docs/operating-system/` | When does learning happen | Daily Operating System's evening/Sunday windows |
| `docs/learning-system/` (this folder) | **What** gets learned, in what order, and how mastery is actually tracked | The real 62-day, 6-phase roadmap |
| `templates/` | Fill-in artifact shapes | `mastery-rubric-template.md` — one blank rubric per concept |

## The Documents

| Document | Covers |
|---|---|
| [`roadmap.md`](roadmap.md) | The master 62-day, six-phase bootcamp roadmap |
| [`knowledge-map.md`](knowledge-map.md) | The overall DS/ML/AI Engineering domain map |
| [`daily-learning-plan.md`](daily-learning-plan.md) | How a single day's learning content is structured |
| [`weekly-learning-plan.md`](weekly-learning-plan.md) | How a week's learning content is structured |
| [`revision-plan.md`](revision-plan.md) | What gets revised and on what phase-linked schedule |
| [`mastery-rubric-methodology.md`](mastery-rubric-methodology.md) | The 5-level mastery methodology used across all concepts |
| [`progress-tracking.md`](progress-tracking.md) | How learning progress rolls up across trackers and reviews |
| [`assessment-guide.md`](assessment-guide.md) | How learning connects to formal assessment |

Learning Journal itself isn't duplicated here — it already exists as `templates/learning-journal-entry-template.md` (the format) and `journal/` (where real entries live).

## Next Steps

- Update `roadmap.md`'s phase-completion status at every phase transition, per `playbooks/learning-new-topic.md`.

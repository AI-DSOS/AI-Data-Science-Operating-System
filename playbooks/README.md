---
title: playbooks/ — Operational Playbooks
purpose: Step-by-step, checklist-first runbooks for the 10 recurring situations named in the original DSOS scope — distinct from docs/operating-system/ (which defines the policy and cadence) and docs/departments/ (which defines who owns what).
owner: Arulkumaran
dependencies: [AGENTS.md]
related_documents: [docs/master-index.md, docs/operating-system/README.md]
version: 1.0.0
last_updated: 2026-07-03
---

## Table of Contents

- [Overview](#overview)
- [Playbooks vs. Operating System vs. Departments](#playbooks-vs-operating-system-vs-departments)
- [The 10 Playbooks](#the-10-playbooks)
- [Next Steps](#next-steps)

## Overview

A playbook answers "what do I literally do, in order, right now" — no policy discussion, no rationale beyond a one-line pointer, just numbered steps. This folder was named in `AGENTS.md` Section 3 from Phase 1 but never built across any of the first 10 phases; it's delivered here as a v1.1 module.

## Playbooks vs. Operating System vs. Departments

| Layer | Answers | Example |
|---|---|---|
| `docs/departments/` | Who owns this, what are the KPIs | Learning Mentor owns bootcamp study |
| `docs/operating-system/` | What's the policy, how often, why | Weekly Review's agenda and decision rules |
| `playbooks/` (this folder) | What do I do, step by step, right now | "Open the tracker. Check phase status. Write 3 bullets. Done." |

Two playbooks (Weekly Review, Monthly Board Meeting) deliberately overlap in name with existing `docs/operating-system/` documents — those define the *what and why*; the playbook versions here are the compressed *checklist* version for actually running the session without re-reading the full policy doc each time.

## The 10 Playbooks

| # | Playbook | For |
|---|---|---|
| 1 | [Learning a New Topic](learning-new-topic.md) | Learning Mentor |
| 2 | [Starting a New Project](starting-new-project.md) | Enterprise Project Architect |
| 3 | [Debugging Production Issues](debugging-production-issues.md) | Enterprise Project Architect |
| 4 | [Preparing for Interviews](preparing-for-interviews.md) | Technical Interviewer |
| 5 | [Publishing a GitHub Repository](publishing-github-repository.md) | Career & Personal Brand Coach |
| 6 | [Writing Technical Articles](writing-technical-articles.md) | Career & Personal Brand Coach |
| 7 | [Building a Portfolio](building-a-portfolio.md) | Career & Personal Brand Coach |
| 8 | [Planning a Sprint](planning-a-sprint.md) | CTO / Enterprise Project Architect |
| 9 | [Running a Weekly Review](weekly-review.md) | CTO |
| 10 | [Running a Monthly Board Meeting](monthly-board-meeting.md) | CTO |

## Next Steps

- Revise any playbook that doesn't hold up once actually run a few times — a playbook that's never been executed is a guess, not a proven runbook. Track this at the first post-v1.1 Quarterly Review.

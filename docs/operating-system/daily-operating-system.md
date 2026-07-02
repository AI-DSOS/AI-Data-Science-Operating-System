---
title: Daily Operating System
purpose: Defines the structure of a single day within DSOS — how the fixed job, evening study window, and Sunday deep-dive window are used, and what gets logged.
owner: Arulkumaran
dependencies: [AGENTS.md, docs/departments/README.md]
related_documents: [docs/operating-system/README.md, docs/operating-system/time-blocking.md, docs/operating-system/deep-work.md, docs/departments/learning-mentor.md]
version: 0.1.0
last_updated: 2026-07-02
---

## Table of Contents

- [Overview](#overview)
- [Weekday Structure](#weekday-structure)
- [Sunday Structure](#sunday-structure)
- [What Gets Logged Daily](#what-gets-logged-daily)
- [Decision Rules](#decision-rules)
- [Checklist](#checklist)
- [References](#references)
- [Next Steps](#next-steps)

## Overview

There is one non-negotiable constraint: Synechron/Morgan Stanley QA work occupies daytime hours. Everything in this document happens in the remaining windows — weekday evenings and Sunday. The goal isn't to maximize hours; it's to protect the windows that exist from fragmentation.

## Weekday Structure

| Block | Activity | Owning department |
|---|---|---|
| Daytime | Synechron QA automation work (not part of DSOS) | — |
| Evening (primary window) | Bootcamp study session per the 62-day plan | Learning Mentor |
| Evening (if time remains) | Portfolio project work, or content drafting | Enterprise Project Architect / Career & Personal Brand Coach |

Only one evening block is guaranteed. If the evening is short, the bootcamp session takes priority over everything else — see Decision Rules.

## Sunday Structure

Sunday is the deep-dive window — the only day with enough contiguous time for multi-hour focused work per `deep-work.md`.

| Block | Activity |
|---|---|
| Deep-dive session 1 | Hardest/most multi-part bootcamp topic of the week |
| Deep-dive session 2 | Portfolio project implementation (Enterprise Project Architect) |
| Light session | Mock interview (Technical Interviewer) or content/pipeline work (Career & Personal Brand Coach), whichever is due that week |
| Reserve | Vaagai business development, only if the week's bootcamp and project targets are on track (see Decision Rules) |

## What Gets Logged Daily

- One learning journal entry (concept, confidence score) — even on days with no formal study session, log "no session" rather than leaving a gap.
- Any blocker or escalation raised to the CTO department.
- Any project milestone advanced.

## Decision Rules

- Bootcamp study always outranks portfolio-project work on weekday evenings when time is short — the Aug 15 deadline is concept-mastery-driven, not project-count-driven.
- Vaagai work only happens in the Sunday reserve block, and only if that week's bootcamp phase tracker is on schedule (per `docs/departments/learning-mentor.md` escalation rule: >3 days behind triggers a stop on Vaagai time until caught up).
- A missed evening session is not made up by cramming the next day — it's absorbed into the following Sunday's deep-dive instead, to avoid burnout-driven low-quality sessions.

## Checklist

- [ ] Evening session identified (bootcamp, project, or explicitly "none" — no silent skips)
- [ ] Journal entry logged
- [ ] Sunday blocks allocated per the priority order above
- [ ] Any blocker escalated, not just noted

## References

- Krish Naik bootcamp study plan (62-day, six-phase, June 15 – Aug 15)
- `docs/departments/learning-mentor.md` — owns the bootcamp tracker this schedule follows

## Next Steps

- Link this document to a daily tracker template once `templates/` exists (Phase 5).

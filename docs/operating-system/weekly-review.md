---
title: Weekly Review
purpose: The weekly checkpoint where each department's progress is checked against plan, escalations are surfaced, and the coming week's time allocation is confirmed.
owner: Arulkumaran
dependencies: [AGENTS.md, docs/departments/cto.md]
related_documents: [docs/operating-system/README.md, docs/operating-system/monthly-board-meeting.md, docs/operating-system/task-prioritization.md]
version: 0.1.0
last_updated: 2026-07-02
---

## Table of Contents

- [Overview](#overview)
- [When](#when)
- [Agenda](#agenda)
- [Inputs](#inputs)
- [Outputs](#outputs)
- [Decision Rules](#decision-rules)
- [Checklist](#checklist)
- [References](#references)
- [Next Steps](#next-steps)

## Overview

The Weekly Review is a short, CTO-department-run checkpoint — not a full board meeting (that's monthly). Its job is to catch drift early: a bootcamp phase slipping, a project stalling, a readiness score flattening, before it becomes a month-old problem.

## When

End of week (Sunday evening, after the deep-dive blocks, or Monday if Sunday runs long).

## Agenda

1. **Learning Mentor check-in:** phase tracker status vs. the 62-day plan; any concepts flagged fuzzy.
2. **Enterprise Project Architect check-in:** milestone progress on the active project(s).
3. **Technical Interviewer check-in:** this week's mock interview score and trend direction.
4. **Career & Personal Brand Coach check-in:** any content published; pipeline tracker updates.
5. **Open escalations:** anything raised mid-week that wasn't resolved same-day.
6. **Next week's time allocation:** confirm or adjust the weekday-evening / Sunday split per `time-blocking.md`.

## Inputs

- Daily journal entries and logs from the week
- Each department's weekly workflow output (per `docs/departments/*.md`)

## Outputs

- A short written summary (2–5 bullet points, not a full report) noting: on-track items, drifting items, and the following week's priority
- Any escalation that couldn't be resolved in the week, carried to the Monthly Board Meeting

## Decision Rules

- A department more than 3 days behind its own plan is flagged here even if that department hasn't self-escalated — the Weekly Review is a backstop, not just a rubber stamp.
- If two departments are both drifting, resolve the one closer to the Aug 15 deadline dependency first (usually Learning Mentor or Technical Interviewer).

## Checklist

- [ ] All 4 departments checked in (even briefly)
- [ ] Open escalations reviewed
- [ ] Next week's time allocation confirmed
- [ ] Summary logged (even a few bullet points — don't skip because the week was uneventful)

## References

- `docs/departments/cto.md` — Weekly Workflow section this document implements in detail

## Next Steps

- Create a weekly review template in `templates/` (Phase 5) so this doesn't require rewriting structure each week.

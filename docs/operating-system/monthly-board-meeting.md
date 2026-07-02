---
title: Monthly Board Meeting
purpose: The monthly checkpoint where all five departments formally report KPIs and blockers, the v1.0 scorecard is reconciled, and the next month's priorities are set.
owner: Arulkumaran
dependencies: [AGENTS.md, docs/departments/cto.md]
related_documents: [docs/operating-system/README.md, docs/operating-system/weekly-review.md, docs/operating-system/quarterly-review.md, docs/progress/v1-scorecard.md]
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

The "board meeting" framing is deliberate: this is the one point in the cadence where every department reports formally, as if to a board, rather than just checking in informally. It's the CTO department's primary governance mechanism (per `docs/departments/cto.md`).

## When

Last weekend of the calendar month, replacing that week's Weekly Review (not in addition to it).

## Agenda

1. **Learning Mentor report:** phase completion vs. plan, mastery rubric roll-up, concepts handed off to other departments.
2. **Enterprise Project Architect report:** projects advanced/completed this month, honest metric results, engineering standards compliance.
3. **Technical Interviewer report:** readiness score trend for the month, question bank growth, gaps routed elsewhere.
4. **Career & Personal Brand Coach report:** content published, pipeline status (recruiter conversations, interviews scheduled).
5. **Scorecard reconciliation:** CTO checks `docs/progress/v1-scorecard.md` against actual repo state; corrects drift.
6. **Roadmap check:** confirm the current Phase (per `AGENTS.md` Section 10) is still the right priority, or document a deviation.
7. **Next month's priorities:** one headline priority per department.

## Inputs

- Four weeks of Weekly Review summaries
- `docs/progress/v1-scorecard.md` and `docs/CHANGELOG.md`
- Any carried-over escalations from the month's weekly reviews

## Outputs

- Board meeting minutes (dated, one per month) — location TBD once `templates/` exists (Phase 5); until then, log as a dated entry appended to this file or a simple `docs/operating-system/board-minutes/` folder created on first use
- Reconciled scorecard
- Documented roadmap deviations, if any
- Next month's headline priority per department

## Decision Rules

- The scorecard reconciliation happens every month without exception — a stale scorecard is a CTO-level quality gate failure per `docs/departments/cto.md`.
- If August 15 readiness is at risk based on the trend across the month's four weekly reviews, this is the point where a real reprioritization decision gets made (e.g., pausing Vaagai work, adding a weekday deep-work session) — not deferred to the next month.

## Checklist

- [ ] All 5 departments reported (4 operational + CTO's own reconciliation)
- [ ] Scorecard reconciled against actual repo state
- [ ] Roadmap phase confirmed or deviation documented
- [ ] Next month's priorities set, one per department
- [ ] Minutes logged

## References

- `docs/departments/cto.md` — Monthly Workflow section this document implements in detail
- `docs/progress/v1-scorecard.md`

## Next Steps

- Create `docs/operating-system/board-minutes/` on the first real monthly meeting, rather than pre-creating an empty folder now.
- Create the board meeting agenda/minutes template in `templates/` (Phase 5).

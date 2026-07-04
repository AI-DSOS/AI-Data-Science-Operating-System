---
title: Playbook — Running a Monthly Board Meeting
purpose: The compressed, checklist-only version of running a Monthly Board Meeting — see docs/operating-system/monthly-board-meeting.md for the full policy and reasoning.
owner: Arulkumaran
dependencies: [docs/operating-system/monthly-board-meeting.md]
related_documents: [playbooks/README.md, templates/monthly-board-meeting-template.md]
version: 1.0.0
last_updated: 2026-07-03
---

## When to Use
Last weekend of the calendar month, replacing that week's Weekly Review, per `docs/operating-system/monthly-board-meeting.md`.

## Steps

1. Copy `templates/monthly-board-meeting-template.md`.
2. Pull all 4 Weekly Review summaries from the month.
3. Write each department's formal report section (Learning Mentor, Enterprise Project Architect, Technical Interviewer, Career & Personal Brand Coach).
4. Run `prompts/repository-maintenance/scorecard-reconciliation.md` against `docs/progress/v1-scorecard.md` — actually re-count files, don't trust the running total.
5. Run `prompts/repository-maintenance/phase-roadmap-check.md` to confirm the current priority is still right.
6. Set one headline priority per department for next month.
7. Save the minutes, dated.

## Checklist

- [ ] All 4 departments reported
- [ ] Scorecard reconciled against actual file counts, not assumed accurate
- [ ] Roadmap phase confirmed or deviation documented
- [ ] Next month's priorities set

## References

- `docs/operating-system/monthly-board-meeting.md` — the full policy this playbook compresses
- `docs/progress/v1-hardening-report.md` — an example of what real reconciliation looks like

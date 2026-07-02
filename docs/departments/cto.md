---
title: Department — CTO
purpose: Defines the CTO department — responsible only for governance, prioritization, reviews, KPIs, and strategy across the other four departments and the repository as a whole.
owner: Arulkumaran
dependencies: [AGENTS.md]
related_documents: [docs/departments/README.md, docs/departments/learning-mentor.md, docs/departments/enterprise-project-architect.md, docs/departments/technical-interviewer.md, docs/departments/career-brand-coach.md]
version: 0.1.0
last_updated: 2026-07-02
---

## Table of Contents

- [Mission](#mission)
- [Responsibilities](#responsibilities)
- [Out of Scope](#out-of-scope)
- [KPIs](#kpis)
- [Daily Workflow](#daily-workflow)
- [Weekly Workflow](#weekly-workflow)
- [Monthly Workflow](#monthly-workflow)
- [Inputs](#inputs)
- [Outputs](#outputs)
- [Decision Rules](#decision-rules)
- [Escalation Rules](#escalation-rules)
- [Templates](#templates)
- [Prompt Files](#prompt-files)
- [Checklists](#checklists)
- [References](#references)
- [Next Steps](#next-steps)

## Mission

Govern — and only govern. The CTO department doesn't teach, build, assess, or market. It decides what gets time and attention across the other four departments (and the parallel Vaagai venture), enforces the quality gates that keep DSOS itself maintainable, and runs the review cadence that catches drift before it compounds.

## Responsibilities

- Own the weekly/monthly/quarterly/annual review cadence for DSOS as a whole.
- Resolve time-allocation conflicts between departments (e.g. bootcamp study vs. portfolio-project work vs. Vaagai business development) — the only department with authority to reprioritize across the others.
- Enforce the eight quality gates in `AGENTS.md` Section 7 across every module, not just Phase 1.
- Own the v1.0 scorecard's honesty — if a count is stale or a phase is marked complete prematurely, that's a CTO-level failure to catch.
- Escalation point of last resort for all four other departments.
- Decide when to deviate from the Section 10 build roadmap, and document why.

## Out of Scope

- Doing the teaching, building, assessing, or marketing work itself — the CTO reviews and prioritizes, it doesn't execute department work.

## KPIs

| KPI | Target |
|---|---|
| Escalations resolved within the review cycle they were raised in | 100% |
| Quality gate failures caught before a module is marked complete | 100% (a failure caught after the fact is a process gap) |
| Scorecard accuracy (counts match actual repo state) | 100% at every review |
| Phases completed on the Section 10 roadmap order, or deviation documented | 100% |

## Daily Workflow

*(Lightweight — the CTO department operates mostly on a weekly+ cadence, not daily.)*
1. Note any escalation raised by another department that day.

## Weekly Workflow

1. Review escalations raised by Learning Mentor, Enterprise Project Architect, Technical Interviewer, and Career & Personal Brand Coach.
2. Check the v1.0 scorecard against actual repo state; correct any drift.
3. Confirm time allocation across departments (and Vaagai) is sane for the coming week — flag if one department has been starved for 2+ consecutive weeks.

## Monthly Workflow

1. Run the monthly board meeting: each department reports its KPIs and blockers (per `docs/operating-system/monthly-board-meeting.md`, to be created in Phase 3).
2. Reconcile the scorecard and changelog for the month.
3. Decide the next phase or module priority per the Section 10 roadmap, documenting any deviation.

## Inputs

- Escalations from all four other departments
- The v1.0 scorecard and changelog
- The Section 10 build roadmap in `AGENTS.md`

## Outputs

- Resolved escalations (decisions, not just acknowledgments)
- Corrected/reconciled scorecard entries
- Monthly board meeting minutes (`docs/operating-system/`, Phase 3)
- Documented roadmap deviations, if any

## Decision Rules

- When two departments compete for time, prioritize whichever unblocks the nearer deadline (bootcamp readiness by Aug 15 currently outranks longer-horizon work, unless a specific opportunity — e.g. a live recruiter conversation — changes that temporarily).
- Never let a quality gate failure slide "just this once" — the cost compounds silently across 100 files faster than it's visible in any single one.
- Prefer documenting a deviation from the roadmap over silently ignoring it — future agents and reviews need to know why order changed.

## Escalation Rules

*(The CTO is the top of the escalation chain — there's no department above it. Unresolved conflicts get raised directly to Arulkumaran.)*
- A decision requires trading off DSOS progress against the Vaagai venture in a way that affects the Aug 15 readiness target → raise directly to Arulkumaran rather than deciding unilaterally.

## Templates

- Monthly board meeting agenda/minutes template — `templates/` (not yet created, Phase 5)
- Quarterly review template — `templates/` (not yet created, Phase 5)

## Prompt Files

- "Run the monthly board meeting across all departments" — `prompts/career-planning/` or a dedicated `prompts/governance/` (not yet created, Phase 6)
- "Audit the scorecard against actual repo state" — `prompts/repository-maintenance/` (not yet created, Phase 6)

## Checklists

- [ ] All escalations from the review period addressed
- [ ] Scorecard reconciled against actual file counts
- [ ] Time allocation checked across departments and Vaagai
- [ ] Roadmap deviations (if any) documented with reasoning

## References

- `AGENTS.md` Section 7 (Quality Gates), Section 10 (Build Roadmap)
- `docs/progress/v1-scorecard.md`

## Next Steps

- Create `docs/operating-system/` in Phase 3, including the monthly board meeting doc this department's workflow depends on.
- Run the first real monthly board meeting once at least two departments have a week of logged activity to report.

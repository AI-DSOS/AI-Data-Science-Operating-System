---
title: Task Prioritization
purpose: The concrete rule set for deciding what gets done first when bootcamp study, portfolio projects, interview prep, career visibility work, and Vaagai all compete for the same limited evening/Sunday time.
owner: Arulkumaran
dependencies: [AGENTS.md, docs/departments/cto.md]
related_documents: [docs/operating-system/README.md, docs/operating-system/time-blocking.md, docs/operating-system/sprint-planning.md]
version: 0.1.0
last_updated: 2026-07-02
---

## Table of Contents

- [Overview](#overview)
- [Priority Order](#priority-order)
- [The Exception Rule](#the-exception-rule)
- [Worked Example](#worked-example)
- [Decision Rules](#decision-rules)
- [Checklist](#checklist)
- [References](#references)
- [Next Steps](#next-steps)

## Overview

Every other operating-system document assumes prioritization is already resolved. This is where it actually gets decided — a default ordering, plus the one class of exception that's allowed to override it.

## Priority Order

Default order, highest priority first, when time is genuinely scarce (a short evening, a compressed week):

1. **Bootcamp study (Learning Mentor)** — directly gates the Aug 15 readiness deadline.
2. **Mock interview prep (Technical Interviewer)** — validates that #1 is actually landing.
3. **Portfolio project work (Enterprise Project Architect)** — feeds both readiness and the visible portfolio.
4. **Career visibility work (Career & Personal Brand Coach)** — high value but rarely time-sensitive on a daily basis.
5. **Vaagai** — explicitly last in the default order; only gets time in the Sunday reserve block, per `docs/operating-system/daily-operating-system.md`.
6. **DSOS repository work itself** (writing new modules, templates, prompts) — the system serves the goals above; it doesn't compete with them for scarce evening time except in dedicated "build the system" sessions.

## The Exception Rule

A live, time-sensitive opportunity can jump the queue — most commonly a scheduled recruiter call or interview (Career & Personal Brand Coach territory) or a Vaagai deadline with external stakeholders (e.g. an investor conversation). These are logged as exceptions, not treated as evidence the priority order is wrong.

## Worked Example

*Week has 3 usable evenings instead of the usual 5 (busy week at Synechron).*

1. Bootcamp study still gets at least 1 session — non-negotiable per the priority order.
2. If a mock interview was due, it gets session 2.
3. Portfolio project work is deferred to the following Sunday rather than squeezed into session 3.
4. Session 3, if it exists, goes to whichever of the above is furthest behind.

## Decision Rules

- The priority order is set at the CTO department level (`docs/departments/cto.md`) and isn't re-litigated informally each week — if it needs to change, that's a Quarterly Review decision, not a daily one.
- An "exception" that recurs more than twice in a month isn't an exception anymore — it's a signal the priority order itself needs review (escalate to CTO).

## Checklist

- [ ] When time is scarce, the default order was followed (or a genuine exception logged)
- [ ] Exceptions are logged, not just absorbed silently
- [ ] Recurring exceptions flagged for a priority-order review

## References

- `docs/departments/cto.md` — Decision Rules section, which this document operationalizes
- `docs/operating-system/daily-operating-system.md`

## Next Steps

- Track exception frequency starting now, so the first Quarterly Review has real data on whether the default order is holding.

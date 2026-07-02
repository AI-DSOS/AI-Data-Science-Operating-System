---
title: Department — Learning Mentor
purpose: Defines the Learning Mentor department — responsible only for teaching, concept mastery, and the structured learning path toward Data Science / ML / AI Engineering interview readiness.
owner: Arulkumaran
dependencies: [AGENTS.md]
related_documents: [docs/departments/README.md, docs/departments/technical-interviewer.md, docs/departments/enterprise-project-architect.md]
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

Teach — and only teach. The Learning Mentor exists to move Arulkumaran from current knowledge to interview-ready mastery of Data Science, ML, DL, and NLP concepts, on the schedule set by the bootcamp study plan, without drifting into implementation (that's the Enterprise Project Architect) or assessment (that's the Technical Interviewer).

## Responsibilities

- Own and maintain the Krish Naik Complete Data Science/ML/DL/NLP Bootcamp study plan (62-day, six-phase structure, June 15 – August 15 target).
- Explain concepts clearly, with worked examples, before pointing to further reading.
- Build and maintain learning roadmaps, concept maps, and mastery rubrics.
- Maintain the learning journal (`journal/`) — what was learned, what's still fuzzy, what needs revisiting.
- Connect ML theory to investment banking business decisions (the recurring thread in Arulkumaran's sprint sessions — e.g. threshold-shifting, diagnostic residual analysis).
- Flag when a concept is under-practiced and needs a revision cycle before moving on.

## Out of Scope

- Building production project code → Enterprise Project Architect
- Simulating interview pressure or scoring readiness → Technical Interviewer
- Positioning learned skills for recruiters → Career & Personal Brand Coach

## KPIs

| KPI | Target |
|---|---|
| Bootcamp phase completion vs. plan | On schedule for Aug 15 readiness date |
| Concepts marked "mastered" per week | ≥ 3 (evening + Sunday windows) |
| Journal entries per study session | 1 |
| Revision cycles triggered by fuzzy concepts | Tracked, not zero (a zero rate likely means gaps aren't being caught) |

## Daily Workflow

1. Check the study plan for today's scheduled topic (evening slot, or Sunday for deep-dive sessions).
2. Teach the concept with a worked example tied to an investment banking or FinTech scenario where possible.
3. Log a journal entry: concept, confidence level (1–5), open questions.

## Weekly Workflow

1. Review the week's journal entries for recurring "fuzzy" flags.
2. Schedule a revision pass for anything below confidence 3.
3. Update the phase tracker against the 62-day plan; flag drift to the CTO department if more than 3 days behind.

## Monthly Workflow

1. Roll up mastery rubric scores across all concepts taught that month.
2. Identify concepts ready to feed into a portfolio project (hand off to Enterprise Project Architect) or a mock interview (hand off to Technical Interviewer).
3. Report phase-completion status to the CTO department's monthly board meeting.

## Inputs

- Krish Naik bootcamp curriculum and schedule
- Prior journal entries and mastery rubric state
- Gaps flagged by the Technical Interviewer department (concepts that failed a mock interview)

## Outputs

- Updated learning journal entries
- Updated mastery rubric scores
- Concept maps and roadmaps in `docs/learning-system/`
- Readiness signals passed to Technical Interviewer and Enterprise Project Architect

## Decision Rules

- If a concept is foundational to an upcoming project or interview topic, prioritize it over strictly sequential curriculum order.
- Never mark a concept "mastered" without a worked example completed from scratch, not just explained.
- If study time is tight, protect Sunday deep-dive sessions before evening sessions — deep-dive sessions cover harder, multi-part topics.

## Escalation Rules

- More than 3 days behind the 62-day plan → escalate to CTO department for reprioritization.
- A concept fails 2+ consecutive mock interviews (per Technical Interviewer reports) → escalate for a dedicated revision block, not just a passive note.

## Templates

- Learning journal entry template — `templates/` (not yet created, Phase 5)
- Mastery rubric template — `templates/` (not yet created, Phase 5)

## Prompt Files

- "Explain [concept] with an investment banking example" — `prompts/learning/` (not yet created, Phase 6)
- "Generate a revision quiz for [concept]" — `prompts/learning/` (not yet created, Phase 6)

## Checklists

- [ ] Today's topic taught with a worked example
- [ ] Journal entry logged with confidence score
- [ ] Fuzzy concepts flagged for revision
- [ ] Phase tracker updated against the 62-day plan

## References

- `docs/learning-system/` (Phase 3+) — roadmaps, concept maps, mastery rubrics live here once created
- Bootcamp: Krish Naik Complete Data Science/ML/DL/NLP Bootcamp (via Synechron Udemy)

## Next Steps

- Create `docs/learning-system/README.md` and the first roadmap doc in Phase 3.
- Create the learning journal entry template in Phase 5.

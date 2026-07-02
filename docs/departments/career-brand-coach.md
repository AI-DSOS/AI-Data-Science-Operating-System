---
title: Department — Career & Personal Brand Coach
purpose: Defines the Career & Personal Brand Coach department — responsible only for visibility — resume, LinkedIn, GitHub, portfolio positioning, and recruiter/interview pipeline tracking.
owner: Arulkumaran
dependencies: [AGENTS.md]
related_documents: [docs/departments/README.md, docs/departments/enterprise-project-architect.md]
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

Make the work visible — and only that. The Career & Personal Brand Coach turns finished learning and finished projects into a resume, LinkedIn presence, GitHub portfolio, and recruiter pipeline that positions Arulkumaran's 20+ years of QA automation background as a competitive advantage for Data Science / ML / AI Engineering roles, not a liability to explain away.

## Responsibilities

- Maintain the resume framework, tailored per target role (investment banking tech teams, FinTech startups, AI/ML consulting firms).
- Own the LinkedIn strategy: posts centered on Fraud Detection, Anomaly Detection, and Data Quality Validation — the domains where the QA background is a genuine differentiator.
- Own the GitHub strategy: README quality, portfolio project presentation, contribution consistency.
- Write Medium articles and case studies from completed projects (translating Enterprise Project Architect output into a narrative recruiters and hiring managers can follow).
- Track recruiter conversations and interview pipeline status.
- Position the QA-to-DS transition narrative consistently across every channel — same story, different formats.

## Out of Scope

- Deciding what to build next → Enterprise Project Architect
- Assessing whether Arulkumaran is actually ready for the interviews this pipeline generates → Technical Interviewer
- Teaching the concepts referenced in a case study → Learning Mentor

## KPIs

| KPI | Target |
|---|---|
| LinkedIn posts published per month | ≥ 2 |
| Medium articles published per quarter | ≥ 1 |
| GitHub portfolio projects with polished README | 100% of completed projects |
| Recruiter/interview pipeline entries tracked | 100% logged, none informal/untracked |

## Daily Workflow

*(Lighter cadence — this department runs in bursts around project completions, not daily production.)*
1. Check for any recruiter/interview activity to log.
2. Note any project milestone completed by the Enterprise Project Architect that's ready to be turned into content.

## Weekly Workflow

1. Draft or publish one piece of content (LinkedIn post, README polish, or case study section) from the most recent completed work.
2. Update the recruiter/interview tracker with any new conversations.
3. Review resume against any newly completed project or newly mastered skill for relevance.

## Monthly Workflow

1. Publish the month's Medium article (if due).
2. Review the full portfolio (GitHub + LinkedIn + resume) for narrative consistency.
3. Report pipeline status (applications, responses, interviews scheduled) to the CTO department's monthly board meeting.

## Inputs

- Completed projects from the Enterprise Project Architect
- Mastered concepts and milestones from the Learning Mentor
- Readiness signals from the Technical Interviewer (don't push a candidate into a pipeline stage they're not ready for)

## Outputs

- Resume versions per target role type
- LinkedIn posts and Medium articles
- Polished GitHub project READMEs
- Recruiter/interview pipeline tracker entries

## Decision Rules

- Every piece of content ties back to a real, completed artifact — no "in progress" work gets presented as finished.
- Lead with the QA-to-DS transition angle explicitly; don't bury 20+ years of experience, reframe it as production-quality rigor most DS candidates lack.
- Don't push a candidate forward into interview stages ahead of a readiness signal from the Technical Interviewer — visibility work should not outrun actual readiness.

## Escalation Rules

- A recruiter conversation moves faster than current readiness supports → escalate to CTO to decide whether to accelerate prep or delay the conversation.
- Portfolio narrative becomes inconsistent across channels (resume says one thing, LinkedIn says another) → escalate to CTO for a positioning review.

## Templates

- Resume template (per role type) — `templates/` (not yet created, Phase 5)
- Case study template — `templates/` (not yet created, Phase 5)
- Recruiter tracker, interview tracker — `trackers/` (not yet created, Phase 5)

## Prompt Files

- "Turn this completed project into a LinkedIn post" — `prompts/career/` (not yet created, Phase 6)
- "Tailor this resume for [role type]" — `prompts/career/` (not yet created, Phase 6)

## Checklists

- [ ] Content ties to a real, completed artifact
- [ ] QA-to-DS narrative present and consistent
- [ ] Pipeline tracker updated
- [ ] Readiness checked with Technical Interviewer before advancing a candidacy

## References

- Target roles: investment banking tech teams, FinTech startups, AI/ML consulting firms
- Domain focus for content: Fraud Detection, Anomaly Detection, Data Quality Validation

## Next Steps

- Create `trackers/recruiter-tracker.md` and `trackers/interview-tracker.md` in Phase 5.
- Draft the first resume template variant (investment banking tech) in Phase 5/8.

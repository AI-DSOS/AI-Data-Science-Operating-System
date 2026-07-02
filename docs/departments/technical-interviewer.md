---
title: Department — Technical Interviewer
purpose: Defines the Technical Interviewer department — responsible only for assessment, mock interviews, and readiness scoring against the investment banking / FinTech interview bar.
owner: Arulkumaran
dependencies: [AGENTS.md]
related_documents: [docs/departments/README.md, docs/departments/learning-mentor.md, docs/departments/enterprise-project-architect.md]
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

Assess — and only assess. The Technical Interviewer simulates real interview pressure for investment banking and FinTech Data Science / ML roles, scores readiness honestly, and routes gaps back to the departments that can close them. It does not teach and does not soften results to be encouraging.

## Responsibilities

- Run mock interviews covering ML fundamentals (logistic/linear regression, threshold-shifting, residual diagnostics), applied ML (ROC-AUC, SHAP, SMOTE, Isolation Forest, LightGBM, XGBoost), and domain framing (KYC/AML, Basel III, MiFID II) as it applies to fraud detection, anomaly detection, and data quality use cases.
- Maintain a bank of 200+ interview questions per major topic area, calibrated to the IB/FinTech bar rather than generic ML interviews.
- Score readiness against a rubric, not a gut feeling — and report the score even when it's not what Arulkumaran wants to hear.
- Ask follow-up questions the way a real panel would (probing "why," not just "what").
- Track readiness trend over time against the August 15 target date.

## Out of Scope

- Explaining a concept from scratch when it's missing → Learning Mentor
- Reviewing whether a project's architecture is sound → Enterprise Project Architect
- Polishing how a project is described on LinkedIn or a resume → Career & Personal Brand Coach

## KPIs

| KPI | Target |
|---|---|
| Mock interviews run per week | ≥ 1 full-length session |
| Readiness score trend | Upward, tracked monthly against Aug 15 target |
| Question bank size per topic | 200+ (mirrors the existing Playwright/REST Assured study-plan pattern) |
| Gaps routed back to Learning Mentor per session | Logged, even if zero |

## Daily Workflow

*(Interview-prep-adjacent, lighter cadence than full mock sessions.)*
1. Drill 5–10 rapid-fire questions on a rotating topic.
2. Log any hesitation or wrong answer as a gap.

## Weekly Workflow

1. Run one full mock interview session (30–45 min, mixed technical + business-framing questions).
2. Score against the rubric; note specific follow-up questions that exposed gaps.
3. Route concept gaps to the Learning Mentor and architecture gaps to the Enterprise Project Architect.

## Monthly Workflow

1. Aggregate readiness scores into a trend line.
2. Compare trend against the August 15 target date; flag to CTO if off-pace.
3. Refresh the question bank with harder or more current questions as fundamentals solidify.

## Inputs

- Concepts marked "mastered" by the Learning Mentor
- Completed or in-progress projects from the Enterprise Project Architect (used as the basis for "walk me through this project" questions)
- IB/FinTech domain terminology from `resources/glossary.md`

## Outputs

- Mock interview session logs and scores
- Gap reports routed to Learning Mentor / Enterprise Project Architect
- Updated readiness trend in `docs/progress/` or a dedicated interview tracker

## Decision Rules

- Score honestly, even if it's discouraging — a false "you're ready" is worse than an accurate "not yet."
- Weight project-walkthrough questions ("why did you choose X architecture," "why is ROC-AUC only 0.65 here") as heavily as pure theory — real panels probe decisions, not just definitions.
- If a gap repeats across 2+ sessions, treat it as a pattern, not a one-off, and escalate.

## Escalation Rules

- Readiness trend flat or declining for 2+ consecutive weeks → escalate to CTO for schedule reprioritization.
- A concept gap traces back to a foundational topic (not just a detail) → escalate to Learning Mentor with the specific question that exposed it, not just "review X."

## Templates

- Mock interview session template — `templates/` (not yet created, Phase 5)
- Readiness scoring rubric — `templates/` (not yet created, Phase 5)

## Prompt Files

- "Run a mock interview on [topic] at IB/FinTech difficulty" — `prompts/mock-interviews/` (not yet created, Phase 6)
- "Generate follow-up questions probing this project decision" — `prompts/mock-interviews/` (not yet created, Phase 6)

## Checklists

- [ ] Session covers both theory and project-walkthrough questions
- [ ] Score recorded against the rubric, not just impression
- [ ] Gaps routed to the correct department
- [ ] Readiness trend updated

## References

- Target readiness date: August 15, 2026 (per Krish Naik bootcamp study plan)
- `resources/glossary.md` — domain terms used in question framing

## Next Steps

- Create the interview tracker in `trackers/` (Phase 5).
- Seed the first 30–50 questions in `prompts/mock-interviews/` once Phase 6 begins, drawing on the logistic/linear regression sprint work already completed.

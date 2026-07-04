---
title: Playbook — Learning a New Topic
purpose: The exact steps to follow when starting a new bootcamp topic.
owner: Arulkumaran
dependencies: [docs/departments/learning-mentor.md]
related_documents: [playbooks/README.md, docs/learning-system/roadmap.md, templates/learning-journal-entry-template.md]
version: 1.0.0
last_updated: 2026-07-03
---

## When to Use
Starting any new concept in the bootcamp schedule — evening session or Sunday deep dive.

## Steps

1. Check `docs/learning-system/roadmap.md` for today's scheduled topic and which phase it belongs to.
2. Use `prompts/learning/explain-with-ib-example.md` to get the concept explained with a worked IB/FinTech example.
3. Attempt a worked example from scratch before checking the answer — use `prompts/learning/worked-example-from-scratch.md`.
4. Copy `templates/learning-journal-entry-template.md` into `journal/`, fill it in: concept, confidence score (1–5), open questions.
5. If confidence < 3, add the concept to this week's revision queue (see `templates/weekly-learning-plan-template.md`).
6. If this is the last topic in a phase, run the Phase Transition Review (`prompts/learning/phase-transition-review.md`) before moving to the next phase.

## Common Pitfalls

- Marking a concept "understood" after reading an explanation but before doing a worked example — don't. Step 3 is not optional.
- Skipping the journal entry on short/rushed sessions — log "short session, low confidence" rather than skipping entirely.

## Checklist

- [ ] Topic identified against the roadmap
- [ ] Explained with a worked example
- [ ] Attempted from scratch, not just reviewed
- [ ] Journal entry logged
- [ ] Revision queue updated if confidence < 3

## References

- `docs/learning-system/roadmap.md`
- `docs/departments/learning-mentor.md`

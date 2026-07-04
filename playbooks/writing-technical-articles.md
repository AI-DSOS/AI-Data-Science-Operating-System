---
title: Playbook — Writing Technical Articles
purpose: The exact steps to follow when drafting a Medium article or long-form technical writeup.
owner: Arulkumaran
dependencies: [docs/career-system/technical-writing-guide.md]
related_documents: [playbooks/README.md, templates/technical-writing-guide-template.md]
version: 1.0.0
last_updated: 2026-07-03
---

## When to Use
A completed project or milestone has a real, honest result worth writing up.

## Steps

1. Check against `docs/career-system/technical-writing-guide.md`'s article selection criteria — is there a real project, an honest result, and a genuine lesson?
2. Draft the outline using `templates/technical-writing-guide-template.md` (or `prompts/technical-writing/project-to-article-outline.md` to generate a first pass).
3. Write the "what didn't work" section first — it's the most commonly skipped and often the most valuable; writing it first prevents it from being cut under time pressure later.
4. Write the rest of the outline.
5. Run `prompts/technical-writing/honest-results-framing.md` on the results section specifically.
6. Run `prompts/technical-writing/editing-for-conciseness.md` on the full draft.
7. Have it reviewed (self-review after a break, minimum) against `prompts/technical-writing/documentation-gap-finder.md`.
8. Publish, then log it in `docs/career-system/README.md`'s cadence tracking (or a future dedicated content tracker) and cross-link it from the relevant project's README.

## Common Pitfalls

- Writing the "clean win" narrative and cutting the honest struggle — the struggle is usually the more valuable part.
- Publishing without an editing pass — first drafts are rarely concise.

## Checklist

- [ ] Real project and honest result behind it
- [ ] "What didn't work" section written, not cut
- [ ] Results framed honestly
- [ ] Edited for conciseness
- [ ] Cross-linked from the project README after publishing

## References

- `docs/career-system/technical-writing-guide.md`

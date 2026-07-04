---
title: Playbook — Starting a New Project
purpose: The exact steps to follow when beginning work on one of the 25 portfolio projects.
owner: Arulkumaran
dependencies: [docs/departments/enterprise-project-architect.md]
related_documents: [playbooks/README.md, projects/README.md, docs/engineering-standards/folder-structure.md]
version: 1.0.0
last_updated: 2026-07-03
---

## When to Use
Moving a project in `projects/` from "blueprint only" to active implementation.

## Steps

1. Re-read the project's existing blueprint README in full — confirm the business problem and architecture are still accurate before writing code.
2. Copy `templates/requirements-template.md` and fill in functional/non-functional requirements if not already detailed.
3. Scaffold the folder structure per `docs/engineering-standards/folder-structure.md` inside the project's own folder.
4. Copy `templates/pyproject-toml-template.md` into the project root.
5. Write the first failing test before the first line of implementation code (per `docs/engineering-standards/testing.md`).
6. Build the baseline model/component first — no complex architecture before a baseline exists (per `docs/engineering-standards/machine-learning.md`).
7. Update the project's status in `projects/README.md`'s index table and `trackers/project-tracker.md` in the same change that starts real work.
8. Log the milestone in `docs/CHANGELOG.md` when the project reaches its next real status (e.g. "Blueprint only" → "Scoped").

## Common Pitfalls

- Starting to code before the requirements are actually written down — resist the urge.
- Building the complex model before the baseline — always baseline first.

## Checklist

- [ ] Blueprint re-confirmed accurate
- [ ] Requirements filled in
- [ ] Folder structure scaffolded to standard
- [ ] First test written before first implementation code
- [ ] Baseline built before anything more complex
- [ ] Status updated in `projects/README.md` and `trackers/project-tracker.md`

## References

- `docs/departments/enterprise-project-architect.md`
- `docs/engineering-standards/folder-structure.md`

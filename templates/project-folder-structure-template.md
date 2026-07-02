---
title: Template — Project Folder Structure Checklist
purpose: Quick-reference checklist to confirm a new project matches engineering-standards/folder-structure.md.
related_documents: [docs/engineering-standards/folder-structure.md]
---

# Folder Structure Checklist: [Project Name]

- [ ] `README.md` at root
- [ ] `pyproject.toml` present
- [ ] `docs/adr/` for architecture decisions
- [ ] `notebooks/` for EDA (numbered, outputs cleared)
- [ ] `src/<project_slug>/` with `training/`, `serving/`, `monitoring/` as applicable
- [ ] `tests/` mirroring `src/`
- [ ] `k8s/` if deployed
- [ ] `Dockerfile` + `.dockerignore`
- [ ] No empty placeholder folders left in

---
title: .github/ — Repository Automation
purpose: Issue/PR templates and CI workflows, including the documentation-site build and deploy pipeline.
owner: Arulkumaran
dependencies: [mkdocs.yml]
related_documents: [README.md, docs/master-index.md]
version: 0.1.0
last_updated: 2026-07-02
---

## Table of Contents

- [Overview](#overview)
- [Contents](#contents)
- [Next Steps](#next-steps)

## Overview

`.github/` holds GitHub-native automation: workflows (CI, doc-site deploy) and, once added, issue/PR templates that enforce the module-report format from `AGENTS.md` Section 5.

## Contents

| File | Purpose | Status |
|---|---|---|
| `workflows/deploy-docs.yml` | Builds `mkdocs.yml` and deploys to GitHub Pages on push to `main` | Created |
| `ISSUE_TEMPLATE/` | Structured issue templates | Not yet created |
| `PULL_REQUEST_TEMPLATE.md` | PR template matching the module-report format | Not yet created |

## Next Steps

- Add `PULL_REQUEST_TEMPLATE.md` mirroring `AGENTS.md` Section 5, rule 6 (folder changes / files added / cross-refs / scorecard update / changelog entry).
- Add a link-checker workflow once the document count is large enough to make manual cross-link validation impractical (rough threshold: Phase 5+).

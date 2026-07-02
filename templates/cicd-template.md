---
title: Template — CI/CD Plan
purpose: Document the continuous integration and deployment pipeline for a project.
related_documents: [docs/engineering-standards/git-github-workflow.md, docs/engineering-standards/testing.md]
---

# CI/CD Plan: [Project Name]

## CI Steps (on every PR)
1. Lint (`ruff`)
2. Type check (`mypy`)
3. Unit + integration tests
4. Dependency vulnerability scan

## CD Steps (on merge to main)
1. Build Docker image
2. Push to registry
3. Deploy to staging
4. [Manual/automatic] promote to production

## Workflow File
`.github/workflows/[name].yml`

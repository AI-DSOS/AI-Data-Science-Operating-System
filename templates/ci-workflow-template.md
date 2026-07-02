---
title: Template — CI Workflow (GitHub Actions)
purpose: Baseline CI workflow for a project repo, per docs/engineering-standards/testing.md.
related_documents: [docs/engineering-standards/testing.md, docs/engineering-standards/git-github-workflow.md]
---

# CI Workflow Template

```yaml
name: CI
on: [push, pull_request]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-python@v5
        with:
          python-version: "3.12"
      - run: pip install uv && uv sync
      - run: uv run ruff check .
      - run: uv run mypy src/
      - run: uv run pytest
```

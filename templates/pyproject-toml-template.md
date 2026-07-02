---
title: Template — pyproject.toml
purpose: Baseline Python project config, per docs/engineering-standards/python.md.
related_documents: [docs/engineering-standards/python.md]
---

# pyproject.toml Template

```toml
[project]
name = "project-slug"
version = "0.1.0"
requires-python = ">=3.12"
dependencies = []

[tool.ruff]
line-length = 100

[tool.mypy]
strict = true

[tool.pytest.ini_options]
testpaths = ["tests"]
```

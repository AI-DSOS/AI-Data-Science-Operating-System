---
title: Engineering Standard — Python
purpose: Baseline Python conventions for all DSOS project code — style, structure, typing, dependency management.
owner: Arulkumaran
dependencies: [AGENTS.md]
related_documents: [docs/engineering-standards/README.md, docs/engineering-standards/testing.md, docs/engineering-standards/naming-conventions.md]
version: 0.1.0
last_updated: 2026-07-02
---

## Table of Contents

- [Overview](#overview)
- [Standard](#standard)
- [Examples](#examples)
- [Checklist](#checklist)
- [References](#references)
- [Next Steps](#next-steps)

## Overview

Python is the primary language across DSOS projects (ML pipelines, FastAPI services, automation scripts). This standard keeps code readable and consistent across 25 projects written over months, by one person plus AI agents.

## Standard

- **Formatting:** `black` (default settings) + `ruff` for linting. No manual style debates — the formatter decides.
- **Typing:** type hints on all function signatures in production code (not required in throwaway EDA notebooks). Use `mypy` in CI for projects tagged production-grade.
- **Dependency management:** `pyproject.toml` + a lockfile (`uv.lock` or `poetry.lock`) per project. No bare `pip install` without pinning in a requirements file.
- **Structure:** `src/` layout for anything beyond a single script — `src/<package_name>/`, `tests/`, `pyproject.toml` at project root.
- **Docstrings:** Google-style docstrings on public functions/classes in production code.
- **Error handling:** no bare `except:` — catch specific exceptions; log before re-raising or handling.

## Examples

```python
def calculate_roc_auc(y_true: list[int], y_pred_proba: list[float]) -> float:
    """Calculate ROC-AUC score for binary classification predictions.

    Args:
        y_true: Ground truth binary labels (0 or 1).
        y_pred_proba: Predicted probabilities for the positive class.

    Returns:
        The ROC-AUC score.
    """
    from sklearn.metrics import roc_auc_score
    return roc_auc_score(y_true, y_pred_proba)
```

## Checklist

- [ ] Formatted with `black`, linted with `ruff`
- [ ] Type hints present on production functions
- [ ] Dependencies pinned via `pyproject.toml` + lockfile
- [ ] `src/` layout used for multi-file projects
- [ ] No bare `except:`

## References

- `docs/engineering-standards/testing.md` — how this code gets tested
- `docs/engineering-standards/naming-conventions.md` — variable/function/module naming

## Next Steps

- Add a `pyproject.toml` template to `templates/` (Phase 5) so every new project starts from the same baseline config.

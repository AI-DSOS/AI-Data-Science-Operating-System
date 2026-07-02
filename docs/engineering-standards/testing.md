---
title: Engineering Standard — Testing
purpose: What "tested" means for DSOS project code — unit, integration, and data/model-specific testing.
owner: Arulkumaran
dependencies: [AGENTS.md]
related_documents: [docs/engineering-standards/README.md, docs/engineering-standards/python.md, docs/engineering-standards/machine-learning.md]
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

Arulkumaran's 20+ years in QA automation is a real advantage here — this standard should reflect that rigor rather than treat testing as an afterthought bolted onto ML code, which is a common (and visible) gap between portfolio projects and production systems.

## Standard

- **Unit tests:** `pytest`, one test file per module, covering business logic — not just "does it run" but "does it produce the right answer for known inputs."
- **Data tests:** schema validation on ingested data (e.g. via `pandera` or `pydantic`) — catch malformed input before it reaches a model, not after a bad prediction is served.
- **Model tests:** a minimum test suite for any trained model — sanity checks (e.g. prediction is within valid range), regression tests (does a known input still produce roughly the expected output after retraining), and fairness/bias spot-checks where the domain calls for it.
- **Integration tests:** for FastAPI services, test the actual HTTP layer (via `TestClient`), not just the underlying functions in isolation.
- **Coverage:** no hard percentage target chased for its own sake — but any function touched by a bug fix gets a regression test added in the same change.
- **CI:** tests run automatically on push/PR for any project with a GitHub Actions workflow (mirrors the DSOS repo's own `deploy-docs.yml` pattern).

## Examples

```python
def test_calculate_roc_auc_perfect_separation():
    y_true = [0, 0, 1, 1]
    y_pred_proba = [0.1, 0.2, 0.8, 0.9]
    assert calculate_roc_auc(y_true, y_pred_proba) == 1.0

def test_calculate_roc_auc_random_predictions():
    y_true = [0, 1, 0, 1]
    y_pred_proba = [0.5, 0.5, 0.5, 0.5]
    assert calculate_roc_auc(y_true, y_pred_proba) == 0.5
```

## Checklist

- [ ] Unit tests cover business logic with known-answer cases
- [ ] Data schema validation in place before model input
- [ ] Model sanity/regression tests exist
- [ ] API integration tests exist for served models
- [ ] CI runs tests automatically

## References

- `docs/engineering-standards/python.md` — where test code lives (`tests/`)
- `docs/engineering-standards/machine-learning.md` — the honest-evaluation standard this testing layer supports

## Next Steps

- Add a `pytest` config + CI workflow template to `templates/` (Phase 5).

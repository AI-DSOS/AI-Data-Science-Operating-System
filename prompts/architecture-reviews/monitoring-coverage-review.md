---
title: Prompt — Monitoring Coverage Review
purpose: Confirm monitoring covers what actually matters, per docs/engineering-standards/mlops.md.
---

## Prompt
```
Review this monitoring setup for {project name}: {paste monitoring plan}.
Does it cover latency, volume, error rate, and drift? What blind spot would
bite us first in production?
```

## Use When
A project's monitoring dashboard is set up but untested against real issues.

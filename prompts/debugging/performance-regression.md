---
title: Prompt — Performance Regression
purpose: Diagnose a service that got slower after a change.
---

## Prompt
```
{Service/endpoint} got slower after {recent change}. Baseline was
{old latency}, now it's {new latency}. What in this change likely caused it?

{paste diff}
```

## Use When
A performance target from templates/performance-and-scalability-related work is missed.

---
title: Prompt — Security-Focused Review
purpose: Review specifically for the anti-patterns in docs/engineering-standards/security.md.
---

## Prompt
```
Review this code only for security issues: secrets, unvalidated input,
non-parameterized queries, missing least-privilege access, or PII handling
gaps. Ignore style issues.

{paste code}
```

## Use When
Any code touching external input, auth, or sensitive data.

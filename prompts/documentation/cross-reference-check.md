---
title: Prompt — Cross-Reference Check
purpose: Verify a document's related_documents links actually resolve, per AGENTS.md Section 7 quality gate.
---

## Prompt
```
Check every link in this document's related_documents field and inline
links. Do they point to real files? List any broken ones.

{paste document}
```

## Use When
Before marking any module complete.

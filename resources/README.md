---
title: resources/ — Glossary, Abbreviations, Reference Library
purpose: Shared vocabulary and reference material used across the repository — checked before writing new documents to avoid duplicate explanations of the same term or concept.
owner: Arulkumaran
dependencies: [AGENTS.md]
related_documents: [resources/glossary.md, docs/master-index.md]
version: 0.1.0
last_updated: 2026-07-02
---

## Table of Contents

- [Overview](#overview)
- [Contents](#contents)
- [How to Add a Term](#how-to-add-a-term)

## Overview

`resources/` holds material that many other documents depend on but none of them own outright: domain terminology, abbreviations, and (as the repo grows) a curated reference library of external material worth linking back to repeatedly.

## Contents

| File | Purpose | Status |
|---|---|---|
| `glossary.md` | Every domain term used more than once across the repo | Skeleton created |
| `abbreviation-guide.md` | Acronym expansions (KYC/AML, MiFID II, ROC-AUC, etc.) | Folded into `glossary.md` for now — split out once it exceeds ~30 entries |
| `reference-library.md` | Curated external references (papers, docs, courses) | Not yet created |

## How to Add a Term

1. Check `glossary.md` first — don't redefine a term that's already there.
2. Add it alphabetically within its category.
3. Keep the definition to 1–2 sentences; link out to a fuller document (e.g. an engineering standard) if more depth is needed.

---
title: journal/ — Learning & Reflection Journal
purpose: Home for daily learning journal entries (per templates/learning-journal-entry-template.md) and weekly/monthly reflection notes (per docs/operating-system/reflection-system.md).
owner: Arulkumaran
dependencies: [templates/learning-journal-entry-template.md, docs/operating-system/reflection-system.md]
related_documents: [docs/master-index.md, docs/departments/learning-mentor.md]
version: 1.0.0
last_updated: 2026-07-03
---

## Table of Contents

- [Overview](#overview)
- [Why This Folder Is Empty of Entries](#why-this-folder-is-empty-of-entries)
- [Naming Convention](#naming-convention)
- [What Goes Here](#what-goes-here)
- [Next Steps](#next-steps)

## Overview

This folder holds two kinds of real, dated entries: daily learning journal entries (concept studied, confidence score, open questions) and periodic reflection notes (is the system itself sustainable, per `docs/operating-system/reflection-system.md`).

## Why This Folder Is Empty of Entries

This folder is scaffolded with its structure and convention, but contains no actual entries. Journal entries are personal, dated records of real study sessions and real reflections — inventing plausible-sounding ones here would misrepresent what's actually happened, which runs against the honest-reporting standard the rest of this repository holds itself to (`docs/engineering-standards/machine-learning.md`). The convention below is ready to use starting with the next real study session.

## Naming Convention

- Daily learning entries: `journal/learning/YYYY-MM-DD.md`
- Weekly reflection notes: `journal/reflection/YYYY-WW.md` (ISO week number)
- Monthly reflection notes: `journal/reflection/YYYY-MM.md`

Subfolders (`learning/`, `reflection/`) are created on first real use, not pre-scaffolded empty here — an empty folder with no content is noise in `git status` and the master index until it holds something real.

## What Goes Here

| Entry type | Template | Trigger |
|---|---|---|
| Daily learning entry | `templates/learning-journal-entry-template.md` | Every study session, per `playbooks/learning-new-topic.md` |
| Weekly reflection | Informal, per `docs/operating-system/reflection-system.md`'s prompts | End of week, folded into Weekly Review |
| Monthly reflection | Informal, per `docs/operating-system/reflection-system.md`'s prompts | End of month, folded into Monthly Board Meeting |

## Next Steps

- Create the first real entry at the next study session, using `templates/learning-journal-entry-template.md` and the naming convention above.
- Once entries exist, `prompts/learning/learning-journal-summarizer.md` can roll up a week's worth for the Weekly Review.

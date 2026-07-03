---
title: Project 22 — Regulatory Reporting Automation
purpose: Formalize the existing Morgan Stanley QFR PDF comparison framework into a documented portfolio project.
owner: Arulkumaran
dependencies: []
related_documents: []
version: 0.6.0
last_updated: 2026-07-02
---

## Status: **Substantially built** (as the standalone `nhecf` package, prior to this repo); not yet migrated into `projects/`

## Business Problem
Automate content extraction and source-target comparison of image-based regulatory fund reports (CAP Partners fund reports: CAP VI, VII, VIII, CAP W50 CV, CAP CV LP), requiring OCR-first architecture.

## Existing Work
A production-ready Python package (`nhecf`) already exists: OCR architecture (OpenCV SSIM, pdfplumber, camelot), tabular/chart/text widget comparison, four reporter types (Excel, JSON, HTML, Console), YAML profile-driven generic architecture supporting 30+ report types, a 153-test suite, and a full CLI.

## Domain Context
Directly demonstrates production-quality engineering applied to a real investment banking regulatory workflow — likely the strongest "this person ships production code" evidence in the portfolio.

## Tech Stack
Python, OpenCV, pdfplumber, camelot, pytest (153 tests).

## Next Steps
Migrate `nhecf` into `projects/tier-3-advanced/22-regulatory-reporting-automation/` with a proper README per `templates/project-readme-template.md`, preserving the existing test suite.

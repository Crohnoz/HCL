# Implementation Guide

This file contains package-application instructions only.

Canonical governance is defined in:

`docs/governance/GOV-001_DOCUMENT_CODING_STANDARD.md`

## Current branch workflow

Apply changes on:

`feature/project-foundation`

Then:

```bash
git status
git add .
git commit -m "docs: address PR-001 governance review findings"
git push
```

The pull request shall target:

`feature/project-foundation` → `develop`

Do not merge this feature branch directly into `main`.

# Apply PR #1 review fixes

Copy this package into the repository root on `feature/project-foundation`.

Then run:

```bash
git status
git add .
git commit -m "docs: address PR-001 governance review findings"
git push
```

In GitHub:

1. Change the PR base from `main` to `develop`.
2. Confirm the updated files.
3. Wait for Sourcery to rerun.
4. Merge into `develop` only after checks pass.

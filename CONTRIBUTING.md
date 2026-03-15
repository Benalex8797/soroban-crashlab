# Contributing to Soroban CrashLab

Thanks for contributing. This project is maintainer-first and contributor-friendly: we optimize for clear issue scope, reproducible changes, and fast review cycles.

## Development setup

### Frontend

```bash
cd apps/web
npm install
npm run dev
```

### Core crate

```bash
cd contracts/crashlab-core
cargo test
```

## Branch and PR flow

1. Create a branch from `main` named `feat/<short-name>` or `fix/<short-name>`.
2. Keep PRs focused on one issue.
3. Link the issue in the PR description using `Closes #<number>`.
4. Include test evidence and reproduction notes for behavior changes.

## Quality bar

- changes are readable and maintainable
- no dead code or placeholder logic in merged PRs
- tests cover the introduced behavior
- docs are updated when user-facing behavior changes

## Review expectations

- maintainers prioritize active Wave issues during the sprint window
- contributors should respond to review comments within 24 hours when possible
- unresolved architectural debates should move to issue discussion to keep PRs focused

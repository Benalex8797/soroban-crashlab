# Maintainer Wave Playbook

This document defines how Soroban CrashLab is operated during Drips Wave cycles.

## Pre-wave checklist

1. Validate that each candidate issue has scope, acceptance criteria, and complexity.
2. Ensure issue labels are consistent:
   - `wave3`
   - `complexity:trivial|medium|high`
   - area labels such as `area:fuzzer`, `area:web`, `area:dx`
3. Confirm issue dependencies are explicit.
4. Keep at least 30 open issues available for contributor allocation.

## Assignment policy

- prioritize first-time contributors on trivial and medium issues
- avoid assigning one contributor to multiple high-complexity issues simultaneously
- if no progress update is posted in 24 hours, request a status check

## PR review policy

Review in this order:

1. correctness and safety
2. deterministic reproducibility of behavior
3. test coverage
4. clarity and maintainability

## Resolution policy

- if work quality is acceptable but merge is blocked for external reasons, resolve per Wave guidance so contributor effort is credited
- move partial work to follow-up issues with clear boundaries

## Post-resolution feedback

- leave practical, direct feedback
- highlight what was done well and what should improve
- keep comments specific to code and collaboration behavior

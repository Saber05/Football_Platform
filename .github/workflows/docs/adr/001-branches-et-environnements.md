# ADR 001: Branches and environments

## Status
Accepted – 2026-11-06

## Context
Solo project built for demonstration. The version shown to agents must be protected.

## Decision
- Three long-lived branches: dev, recette, main (= prod).
- Work branches feature/<JIRA-KEY>-... are squash-merged into dev.
- Promotions dev -> recette -> main through pull requests with a merge commit (never squash).
- Hotfixes start from main (hotfix/<JIRA-KEY>-...) and are merged back into dev.
- One GCP project per environment: dev from S3; rec and prod after week 9.
- Configuration through the FP_ENV variable; the same code runs everywhere.

## Consequences
+ Prod is protected; every step has a quality gate.
- Requires discipline to keep branches from diverging.

## Alternative rejected
Trunk-based development (single branch + tags): lighter, but less readable when
presenting the validation flow expected in companies.
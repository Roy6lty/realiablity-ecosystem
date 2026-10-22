# Project Context — AI & Human Quick Start

> **Read this file first. Then read `docs/STATUS.md` and the active GitHub Issue.**
> Snapshot: 2026-10-12. The project scope is agreed in discussion; code-level completion is not audited.

## Mission

Build a reproducible reliability engineering laboratory where financial, commerce, and utility services exchange realistic traffic. Compare architecture, consistency, resilience, container/orchestrator behavior, deployment strategies, and infrastructure configurations under controlled failures and workloads.

## System map

- **Bank A:** Go + PostgreSQL modular monolith; modules include identity/users, customers, accounts, transfers, transactions, ledger, payments, risk/limits, fees, reconciliation, notifications and audit.
- **Bank B:** independently deployed distributed banking services; interface-compatible scenarios for comparative testing.
- **Commerce:** begin with one shopping app, expand to 2–4 applications with different design patterns.
- **Gateway / switch:** payment routing, states, webhooks, retries, idempotency and reconciliation for inter-system transactions.
- **External:** utility billing; optional delivery or fraud provider.
- **Traffic:** stateful user-behavior bots plus deterministic, controlled distributed load generators.
- **Observability / experiments:** logs, metrics, traces, invariant checks, failure injection, test run metadata and reports.
- **Runtime:** Docker Compose -> Kubernetes -> AWS-like emulation via Floci + Terraform; optional narrowly scoped tests on real AWS.

## Engineering principles

1. Financial correctness is non-negotiable: no duplicate debit/credit, balanced ledger, explicit uncertain states, safe retries.
2. Prefer modular boundaries first; distribute only when an experiment benefits from real service boundaries.
3. Use identical workload profiles and comparable resource allocations for architecture comparisons.
4. Preserve deterministic experiment inputs: version, configuration, dataset, traffic seed, duration and failure schedule.
5. Observe business outcomes, not just HTTP availability.
6. Explicitly distinguish *planned*, *implemented*, *verified* and *released*.
7. Treat AWS emulation as API/workflow validation, not proof of real AWS networking or resiliency behavior.

## Current state (not a completion claim)

- **Architecture and long-term scope:** discussed and recorded.
- **Bank A implementation:** existing Mini Bank development was described in previous conversations (Go/sqlc/pgx/PostgreSQL, core modules, transactional transfer/idempotency); source and test status require inspection before tasks are marked Done.
- **Other systems and advanced phases:** planned until verified otherwise.
- **Current milestone:** P1 — establish a verifiable, well-tested Bank A baseline.
- **Next action:** inspect Mini Bank repo and test results; populate baseline status + open GitHub issues for unresolved gaps.

## Key files

- `docs/STATUS.md` — authoritative human-readable progress snapshot.
- `docs/ROADMAP.md` — milestones and exit criteria.
- `docs/ARCHITECTURE.md` — boundaries and flows.
- `docs/WORK_TRACKING.md` — issue/PR definitions of done, status meanings.
- `docs/DECISIONS/` — architectural decision records.
- `docs/EXPERIMENTS/` — experiment specifications and results.
- `docs/SESSIONS/` — dated handoffs and important meeting notes.

## When an AI starts working

1. Read this file and `docs/STATUS.md`.
2. Read the active Issue, affected module documentation, relevant ADRs and latest matching experiment.
3. Verify the actual repository state and commands before asserting what exists.
4. Make the smallest change with a clear acceptance test.
5. Cite changed files/commits/test output in the issue or PR.
6. Update project status only if a milestone or focus genuinely changed; log new design decisions via ADRs.
7. At the end, report: completed, evidence, known gaps, next step.

Do not guess undocumented repository URLs, infrastructure status, benchmark numbers or release versions.

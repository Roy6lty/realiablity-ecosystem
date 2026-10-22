# ADR-0002: Use a modular monolith as the first financial baseline

- **Date:** 2026-10-12
- **Status:** Proposed / scope agreed, code not audited

## Context

We need reliable financial flows as a baseline for studying distributed architectures. Starting with inter-service transactions would introduce cross-system uncertainty before we establish accounting and transfer semantics.

## Decision

Build/verify Bank A as a Go/PostgreSQL modular monolith, with explicit module ownership, atomic financial operations, ledger invariants, idempotency and reproducible tests. Introduce independently deployed Bank B afterward to compare architecture and failure modes.

## Consequences

Provides a correctness reference and simpler transaction boundary. Bank B will require explicit distributed state machines, recovery and reconciliation rather than assuming cross-service transactions.

## Verification required

Audit current Bank A implementation and link tests to this decision. Update ADR if code reveals a different established architecture.

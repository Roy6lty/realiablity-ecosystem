# EXP-001 — Bank A transfer baseline

**Status:** Draft specification; NOT EXECUTED  
**Date drafted:** 2026-10-12  
**Linked Issue:** pending  
**Target repo + commit SHA:** pending  
**Owner:** pending

## Question

What throughput, latency and resource usage does Bank A exhibit for valid internal transfers, while maintaining financial invariants?

## Workload

- Synthetic sender/receiver accounts with seeded balances.
- Rates: begin conservatively, then step upward until defined saturation criteria occur.
- Include unique transfer references plus separate replay tests.
- Record user model (open-loop arrivals vs closed-loop concurrency), duration, seed and dataset.

## Required telemetry

- Request rate, p50/p95/p99 and error rate.
- DB transaction duration, pool wait time, deadlocks and lock contention.
- CPU/memory/network I/O.
- Ledger imbalance count, duplicate-posting count, unresolved transfer count.

## Pass/fail safety checks

- Accounting entries balance.
- No negative balances when overdrafts are not allowed.
- No double debit for the same idempotency key.
- Final totals are reconciled against seeded amounts/allowed fees.

## Execution record

- Date/time: NOT RUN
- Commands: NOT RUN
- Environment: UNVERIFIED
- Build SHA / digests: UNVERIFIED
- Report links: NONE
- Result: NONE

## Caveats

Avoid claiming performance until the actual environment, load profile and test run are recorded. A failure in the test harness can invalidate an observed bottleneck.

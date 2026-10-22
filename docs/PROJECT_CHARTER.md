# Project Charter

## Problem

Architecture and operational practices are often evaluated through assumptions or isolated benchmarks. We need an instrumented, reproducible multi-system environment where we can test correctness and availability under normal load, stress, partial failure and software/infrastructure change.

## Outcomes

1. Financially correct Bank A baseline (modular monolith).
2. Connected ecosystem with commerce, gateway, utility provider and behavior bots.
3. Distributed Bank B capable of comparable payment/transfer flows.
4. Reproducible experiment runner with observability and permanent findings.
5. Deployment strategy comparison: recreate, rolling, blue-green, canary, shadow where safe, flags, GitOps, rollback.
6. Docker, Kubernetes and AWS-like infrastructure/IaC experiments.

## Non-goals for early phases

- Operating a real financial institution or handling actual funds.
- Building fully featured, commercial-grade e-commerce products.
- Perfectly replicating AWS service behavior locally.
- Adding microservices solely to increase the number of repositories.

## Safety

Use fake users, synthetic money and sandbox integrations. Isolate destructive experiments and restrict CI/CD permissions. Ensure reproducibility and cost controls for optional real-cloud experiments.

## Success metrics

- No ledger imbalance or duplicate postings across validated experiments.
- Demonstrable latency, errors, saturation and recovery plots per test run.
- Traceable decisions and task-to-commit/test-to-experiment evidence.
- A newcomer or AI assistant can read 2 files and identify current phase, next task and sources of truth.

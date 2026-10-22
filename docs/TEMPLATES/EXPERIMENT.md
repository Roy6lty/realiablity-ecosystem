# EXP-NNN — Descriptive title

- Status: Draft / Ready / Running / Completed / Invalidated
- Owner:
- Linked Issue / PR:
- Run ID / date:

## Hypothesis / question

Falsifiable statement and what would count as disconfirmation.

## System under test

Repos/commits, image digests, architecture, dependencies.

## Environment / controls

Hardware, container limits, cluster config, regions (if any), data seed, dataset, versions, services, baselines and cost limits.

## Workload / fault

Generator, open-loop vs closed-loop, arrival rates, concurrency, ramp, duration, fault injection method, timing and rollback controls.

## Safety invariants

Ledger balances, idempotency, valid business states, data retention, blast radius and abort conditions.

## Metrics / collection

Latency distributions, throughput, errors, business correctness, resource saturation, traces, logging and time synchronization.

## Procedure

1. Prepare / seed test data.
2. Verify baseline health and invariants.
3. Run workload and any fault or deployment.
4. Stop safely and reconcile final state.
5. Attach raw data / plots / dashboards.

## Results — complete only after execution

Commands, raw links, observations, anomalies, quantitative results, confidence/limitations.

## Conclusion and follow-up

Was the hypothesis supported? What needs repeating or changing?

# Reliability Experiment Catalogue

**Every experiment must specify both system metrics and business invariants.** Use the [experiment template](TEMPLATES/EXPERIMENT.md).

| ID | Scenario | Hypothesis to test | Essential observations | Status |
| --- | --- | --- | --- | --- |
| EXP-001 | Bank A transfer baseline | Establish repeatable baseline under increasing load | p50/p95/p99, throughput, errors, postings, CPU/DB | Spec drafted |
| EXP-002 | Duplicate transfer requests | Stable idempotency key prevents duplicate financial effects | ledger counts, references, statuses | Planned |
| EXP-003 | Bank A DB latency | Slow DB propagates to transfer latency and pool saturation | pending ops, pools, latency, reconciliation | Planned |
| EXP-004 | Shop payment timeout | Payment uncertainty resolves without double charge | pending payments, callbacks, ledger | Planned |
| EXP-005 | Bank A vs Bank B same workload | Compare overhead and recovery under fixed constraints | latency/resource/error and correctness | Planned |
| EXP-006 | Rolling deployment under load | Graceful termination reduces interruption | in-flight, readiness, errors, rollback | Planned |
| EXP-007 | Blue-green vs canary release | Compare cost, fault exposure and recovery | capacity, errors, affected requests | Planned |
| EXP-008 | Queue worker outage | Backlog accumulates and eventually drains safely | queue lag, retries, poison messages | Planned |
| EXP-009 | Pod kill / node failure | Verify practical recovery behavior | rescheduling, RTO, SLO, lost ops | Planned |
| EXP-010 | Terraform drift | Detect and safely reconcile infra drift | plans, changes, service health | Planned |
| EXP-011 | Floci SQS integration | Validate AWS-like queue API workflow locally | queue delivery, timeouts and limitations | Planned |

## Baseline integrity

Record source commit SHA, container image digests, test dataset, experiment host/resources, load-generator versions, duration, arrival model, concurrency, seed, baseline configuration, failure schedule, and observability links. Avoid comparing results across materially different resource budgets without noting the difference.

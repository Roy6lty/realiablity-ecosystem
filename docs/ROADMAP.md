# Roadmap — outcome based, not date based

Roadmap stages express sequencing, not percent completion. A later workstream (such as instrumentation) may start early.

| ID | Milestone | Acceptance / exit criteria | Status as of 2026-10-12 |
| --- | --- | --- | --- |
| P0 | Scope and operating model | Project charter, architecture sketch, roadmap, tracking policy | Documented; GitHub adoption pending |
| P1 | Bank A correctness baseline | Module ownership audited; tests prove transfer atomicity, ledger balance, idempotency; benchmark runnable | In development; evidence audit pending |
| P2 | First end-to-end ecosystem | One shop + gateway + utility integration + Bank A; synthetic purchase and bill payment flows | Planned |
| P3 | Observability and experiment runner | Trace/metrics/log correlation and repeatable workload definitions; benchmark reports | Planned |
| P4 | Distributed Bank B | Comparable bank APIs; documented cross-service consistency and recovery; architecture benchmark | Planned |
| P5 | Multiple shops and Kubernetes | 2–4 shops; K8s deployments; documented deployment experiments | Planned |
| P6 | Chaos, resilience and release experiments | Fault catalogue, canary/blue-green/rolling comparisons, recovery playbooks, business invariant results | Planned |
| P7 | Terraform + Floci cloud simulation | Reproducible AWS-like IaC modules; supported service integration tests, drift and recovery experiments | Planned |
| P8 (optional) | Real-cloud validation | Cost-limited, explicitly authorized AWS experiments with documented deviations from emulator | Optional |

## Progress rules

- Do not assign a guessed percentage to the overall project.
- Count milestone exit criteria as verified only when backed by commands/tests/PRs/experiment reports.
- For smaller tasks, GitHub Projects is the authoritative work queue.
- Keep immediate focus in `docs/STATUS.md`; make phase changes here when justified.

# Initial Backlog — Issue Candidates

These IDs are **planning identifiers**, not GitHub issue numbers. Convert priorities into actual GitHub Issues and replace with links. “Done” status requires evidence.

| ID | Priority | Phase | Task | Acceptance evidence |
| --- | --- | --- | --- | --- |
| LAB-001 | P0 | P1 | Audit Bank A repository, modules, tests, schemas | Repo commit SHA, test command/output, gap report |
| LAB-002 | P0 | P1 | Formalize account-transfer-ledger invariants | Documented invariants plus executable tests |
| LAB-003 | P0 | P1 | Verify concurrency safety and idempotency | Parallel-transfer and retry test suite |
| LAB-004 | P0 | P1 | Make reproducible local bootstrap | Compose or equivalent, migration and seed instructions |
| LAB-005 | P0 | P1/P3 | Instrument transfer flow | Request metrics, correlation IDs and trace examples |
| LAB-006 | P1 | P2 | Define payment gateway contracts | API schema and state-machine tests |
| LAB-007 | P1 | P2 | Build minimal shop and fake inventory | End-to-end order and payment happy-path test |
| LAB-008 | P1 | P2 | Implement webhook retries and reconciliation | Duplicate/out-of-order webhook tests |
| LAB-009 | P1 | P3 | Define reproducible experiment spec | Seed, dataset, target versions, duration, fault and metrics fields |
| LAB-010 | P1 | P3 | Connect load generator and dashboards | First saved report with trace/log/metric links |
| LAB-011 | P2 | P4 | Write Bank B service-boundary ADR | Approved interfaces, data ownership, failure states |
| LAB-012 | P2 | P4 | Implement Bank B transfer orchestration | Cross-service recovery and reconciliation tests |
| LAB-013 | P2 | P5 | Kubernetes base manifests and health contracts | Repeatable cluster deploy and smoke-test evidence |
| LAB-014 | P2 | P5/P6 | Compare recreate, rolling and blue-green deployment | Same traffic and resources; measured interruption report |
| LAB-015 | P2 | P6 | Implement fault scenarios | Injected fault + measured recovery + invariant checks |
| LAB-016 | P3 | P7 | Integrate Floci + Terraform | Apply/destroy + AWS-like API integration test |
| LAB-017 | P3 | P7 | Infrastructure change and drift experiments | Reproducible IaC diff and experiment report |
| LAB-018 | P3 | P5 | Expand commerce platforms to 2–4 | Defined differences and comparative workload reports |

## Task breakdown rule

Keep issues small enough to finish and verify independently. Prefer one behavior or one experiment per Issue; use epics/milestones to coordinate a large workstream.

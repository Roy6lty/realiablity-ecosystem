# Current Project Status

**Updated:** 2026-10-12  
**Phase:** P1 — Bank A correctness baseline (scoped; code audit needed)  
**Overall project completion:** Not estimated; roadmap scope is still evolving.

## Current focus

Establish a trustworthy baseline for the existing Mini Bank by inspecting the actual code, builds and tests before integrating new components.

## What we know

| Area | State | Evidence / limitation |
| --- | --- | --- |
| Ecosystem requirements | Documented | Discussed and described in this documentation repository |
| Bank A module design | Proposed + some previously described implementation | No current source inspection in this documentation snapshot |
| Bank A transactional transfers and idempotency | Previously described, **not verified here** | Need tests/commit links to establish behavior |
| Shopping platforms | Planned | No implementation evidence recorded |
| Distributed Bank B | Planned | No implementation evidence recorded |
| Load generation / observability | Planned as platform components | Existing separate experiments/tools may be reusable; audit needed |
| Deployment experiments | Planned | No experiment results recorded |
| Floci / Terraform integration | Planned final phase | Validate supported service APIs before designing scenarios |

## Top 3 next actions

1. Identify/confirm the Mini Bank repository, current branch and working baseline; run tests and inspect transfer/ledger code.
2. Open GitHub Issues for gaps in correctness tests, module boundaries and reproducible local startup, with evidence requirements.
3. Establish baseline metrics: traffic scenario, test data setup, p50/p95/p99, errors, resource metrics and ledger invariant checks.

## Active work

No live GitHub Issues have been attached to this starter pack yet. **Do not invent issue IDs.** Add links here after the board is created.

## Blockers / decisions needed

- Confirm repository topology (one ecosystem monorepo vs multiple application repositories); recommendation: one central docs repo and separate app repos as needed.
- Verify current Mini Bank feature implementation and test coverage.
- Choose shared experiment result format/storage and initial observability tooling.

## Last verified evidence

None collected within this new tracking system. First task is to produce an evidence-backed audit.

## Update protocol

When a meaningful milestone changes, revise this file in the same PR as the evidence. Include links to the Issue, PR, commit, CI run or experiment report. Never replace historical experiment results; add new runs.

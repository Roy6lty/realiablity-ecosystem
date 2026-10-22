# Work Tracking and GitHub Setup

## System of record

- **GitHub Projects:** queue, status, priority, iteration, target milestone and owner.
- **GitHub Issues:** problem statement, proposed work and acceptance criteria.
- **Pull requests / commits:** changed implementation and code review.
- **CI / experiments:** evidence of tests and behavior.
- **This repository:** why the architecture exists, current phase, cross-repo decisions, project knowledge, experiments and handoffs.

## GitHub Project recommended fields

- Status: `Backlog`, `Ready`, `In Progress`, `In Review`, `Blocked`, `Done`
- Workstream: `Bank A`, `Bank B`, `Commerce`, `Gateway`, `Bots`, `Experiments`, `Observability`, `Deployments`, `Kubernetes`, `Cloud/IaC`, `Security`
- Phase: `P1` through `P8` (P0 for setup)
- Priority: `P0` critical, `P1` high, `P2` medium, `P3` later
- Complexity: numeric small/medium-sized estimate, optional
- Iteration: weekly or biweekly cadence, optional
- Target milestone: GitHub milestone or single-select field

Views: `Now`, `Roadmap`, `By workstream`, `Blocked`, `Experiments`, `Recently completed`.

## Issue template contract

Every task includes:

1. **Context and intended outcome:** Why is this needed?
2. **Scope:** What will and will not change?
3. **Acceptance criteria:** Behaviors verifiable by tests or observed outcomes.
4. **Dependencies:** Issue and ADR links.
5. **Evidence:** Commands, test output, links to logs/metrics/PRs.

## Definition of Done

- Acceptance criteria satisfied and tested.
- Test output/CI or experiment report attached.
- Financial invariants and safety risks evaluated when applicable.
- Docs / ADR updated if interfaces, design or operations changed.
- PR merged or specified deliverable recorded.
- Issue linked to evidence and marked Done.

**Important:** Work that was discussed, prototyped without tests, or merely merged without meeting criteria is not automatically Done.

## Working cadence

- **At the start of a work session:** read `PROJECT_CONTEXT.md`, `docs/STATUS.md`, active issue, relevant ADRs.
- **During implementation:** leave traceable commits; record unplanned changes as follow-up issues.
- **After implementation:** link PR/CI/test results, update issue status and leave a short handoff.
- **Weekly:** verify board vs reality, archive outdated blockers, update `docs/STATUS.md`, choose 1–3 next tasks.
- **At each significant design change:** create or supersede an ADR.
- **After each experiment:** commit a spec and a run report, preserving raw logs if practical.

## AI session starter prompt

> Read `PROJECT_CONTEXT.md`, `docs/STATUS.md`, and the issue I provide. Summarize the verified current state, the task's acceptance criteria, relevant ADRs and proposed next steps. Inspect repository files before making implementation claims. Do not mark work complete without test evidence. At the end, give an issue-ready progress update, including commands and results.

## Multi-repo guidance

A single docs repo is recommended for cross-system planning. Keep local `README.md`, module docs and root `AGENTS.md` in each application repository. Local agents can use a condensed copy of architectural rules, but the project-wide STATUS and ROADMAP remain centralized. Link the coordination repo from each code repo; don't maintain conflicting copies of the progress status.

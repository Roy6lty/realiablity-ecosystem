# Reliability Engineering Lab

**Status:** Architecture scoped; implementation status awaits code verification  
**Snapshot date:** 2026-10-12  
**Purpose:** An end-to-end, measurable laboratory for distributed systems, banking correctness, infrastructure, deployment strategies, observability, and fault tolerance.

This is the **coordination / documentation repository** for the entire ecosystem. Individual applications may live in separate repositories. Do not copy status information into multiple independently maintained documents.

## Start here

1. [PROJECT_CONTEXT.md](PROJECT_CONTEXT.md) — concise context for humans and AI.
2. [docs/STATUS.md](docs/STATUS.md) — verified progress, current focus, blockers, next actions.
3. [docs/ROADMAP.md](docs/ROADMAP.md) — phases, outcomes and exit criteria.
4. [docs/ARCHITECTURE.md](docs/ARCHITECTURE.md) — system boundaries and interactions.
5. [docs/BACKLOG.md](docs/BACKLOG.md) — proposed initial GitHub Issues (not completed tasks).
6. [docs/WORK_TRACKING.md](docs/WORK_TRACKING.md) — issue, PR, evidence and update rules.
7. [docs/EXPERIMENT_CATALOG.md](docs/EXPERIMENT_CATALOG.md) — reliability study catalogue.
8. [docs/REPOSITORIES.md](docs/REPOSITORIES.md) — repository and deployment inventory.

## Guardrails

- An idea discussed with AI is **proposed**, not implemented.
- A checked-in commit is **implemented**, not necessarily tested.
- Mark work **Done** only with linked evidence and satisfied acceptance criteria.
- Record decisions as ADRs and experiment outcomes in version control.
- Keep production or account secrets out of documentation and AI prompts.

## Suggested GitHub integration

Use one GitHub Project across repositories. Store task implementations as Issues / PRs in the relevant code repository and cross-repo epics in this repository. See [tracking setup](docs/WORK_TRACKING.md).

## Short weekly ritual

Review completed PRs/issues -> verify evidence -> update `docs/STATUS.md` -> refresh `PROJECT_CONTEXT.md` if direction changed -> choose the next 1-3 tasks -> add a dated session summary when an important decision or milestone occurs.

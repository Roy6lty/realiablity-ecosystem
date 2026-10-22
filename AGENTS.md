# Instructions for AI agents working on this project

## Mandatory project context

Before planning or editing, read:
- `PROJECT_CONTEXT.md`
- `docs/STATUS.md`
- the active GitHub Issue / user request
- applicable `docs/DECISIONS/*.md`

For cross-repository work, locate the relevant code repository and verify its current state. This coordination repository is not proof that code exists.

## Working agreement

- Distinguish **proposal**, **code written**, **tests passed**, **deployed**, and **experiment validated**.
- Never mark an Issue complete based solely on conversational agreement.
- Never invent timings, performance measurements, pass/fail outcomes, GitHub issue numbers or CI results.
- Prefer small PRs linked to a task and explicit acceptance criteria.
- Require ledger invariants, idempotency, fault-state recovery and security considerations for financial flows.
- Never run load/chaos tests against shared or production infrastructure without explicit scope and authorization.
- Store synthetic data only; do not commit credentials, access tokens, real PII or payment data.
- If architecture changes, propose an ADR. If an experiment is run, record setup, commands, metrics, limitations, and outcome.
- If a task changes project status, update `docs/STATUS.md` with proof and update date.
- Provide a session handoff with what changed, where, how tested and next steps.

## Standard response at session start

- Current milestone and verified state
- Active task and acceptance criteria
- Planned next action
- Open questions/blockers

## Standard response at session end

- Changes made (paths/commit/PR)
- Tests and evidence
- Open issues / risks
- Next suggested issue
- Docs/status updated? (yes/no/why)

> Notes: `AGENTS.md` is consumed automatically by some coding agents such as Codex. Other AI tools may need these files provided explicitly, so treat it as documentation rather than guaranteed persistent memory.

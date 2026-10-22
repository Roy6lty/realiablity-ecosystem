# ADR-0001: Version-controlled knowledge + GitHub work tracking

- **Date:** 2026-10-12
- **Status:** Proposed for adoption

## Context

The reliability lab spans multiple applications, infrastructure, test rigs and long-lived experiments. We need a reference usable by human contributors and AI agents without reliance on memory or chat history.

## Decision

Use a project-wide documentation/coordination repository. Track live work in GitHub Projects/Issues, implementation in code repositories/PRs, and durable decisions, status and experiments in Git-tracked Markdown.

## Consequences

Pros: version history, linkable evidence, portable AI context, cross-repo status. Costs: someone must keep docs updated; context files can become stale if work is not linked to evidence.

## Verification required

Create repo and GitHub Project; convert initial backlog to issues; confirm status cadence. Mark this ADR Accepted only after adopting it.

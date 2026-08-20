---
name: spec-to-implementation-planner
description: Turn a feature spec, ticket, or rough feature idea into an ordered implementation plan - affected files, sequencing, risk points, and a suggested PR breakdown - before any code is written. Use when the user wants to plan a non-trivial feature or change before implementing it.
---

# Spec-to-Implementation Planner

## Purpose
Jumping straight into code on a non-trivial feature leads to rework: missed edge cases, files touched in the wrong order, one giant unreviewable diff. This skill produces the plan first - grounded in the actual codebase, not a generic template - so implementation is mechanical once the plan is approved.

## When to use
The user has a spec, ticket, or feature idea of meaningful size (more than a one-file fix) and wants a plan before writing code.

## Process
1. **Read the spec/request closely** and extract the concrete requirements versus the ambiguous ones. List open questions separately - do not silently assume answers to ambiguous requirements that materially change the implementation.
2. **Explore the actual codebase** (don't plan against an imagined architecture): locate the relevant modules, existing patterns for similar features, data models, and tests. A plan that ignores existing conventions produces a PR reviewers will reject.
3. **Break the work into ordered steps**, each independently sensible (e.g. data model change → backend logic → API surface → frontend → tests), noting dependencies between steps so the sequence is forced by reality, not arbitrary.
4. **Flag risk points explicitly**: migrations, backward-compatibility concerns, concurrency/race conditions, anything touching auth/permissions/money, and anywhere the spec is ambiguous enough that two reasonable implementations diverge.
5. **Propose a PR breakdown** for the work - one plan-sized change is rarely one PR; suggest natural seams (e.g. schema migration as its own PR, then feature logic, then UI) so review stays tractable.
6. **State what's out of scope** explicitly, to prevent scope creep during implementation.

## Output format
- Requirements (confirmed) vs. open questions (need answers before/during implementation)
- Affected files/modules (from actual codebase exploration, with paths)
- Ordered implementation steps with dependencies
- Risk points
- Suggested PR breakdown
- Explicit out-of-scope list

## Guardrails
Do not fabricate file paths or existing code behavior - explore the actual repository before citing it. If the codebase can't be explored (e.g. no repo access), say so and produce a plan clearly marked as generic/unverified rather than presenting assumptions as findings.

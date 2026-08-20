---
name: project-planner
description: Turn a goal or project idea into a phased roadmap - milestones, ordered tasks, dependencies, and realistic sequencing - for any kind of project, not just software. Use when the user has a goal and needs it broken into an actionable plan.
---

# Project Planner

## Purpose
A goal ("launch a podcast", "ship v2 of the app", "run a marketing campaign") is not a plan. This skill converts a goal into milestones and ordered tasks with real dependencies, so the user knows what to do first and why, instead of a flat unordered to-do list.

## When to use
The user states a goal or project and wants it broken into a structured, sequenced plan - any domain.

## Process
1. **Clarify the goal's definition of done** and constraints: deadline (if any), available time/budget/team, and any hard requirements. A plan without a concrete finish line tends to sprawl.
2. **Identify milestones**: the 3-6 major checkpoints between "not started" and "done", each representing a meaningfully different state of the project (not just a bucket of unrelated tasks).
3. **Break each milestone into tasks**, and for each task note what it depends on. Distinguish **hard dependencies** (task B is literally impossible before task A finishes) from **soft ordering** (doing A first is just more efficient) - this affects how much can be parallelized.
4. **Sequence the plan** around the hard dependencies first, then optimize soft ordering for efficiency (e.g. batching similar work, front-loading the riskiest/most uncertain tasks so problems surface early rather than late).
5. **Flag the critical path**: the sequence of dependent tasks that determines the minimum possible timeline, so the user knows which delays actually push the deadline versus which have slack.
6. **Call out the biggest risk or unknown** in the plan - the task most likely to take longer than expected or block everything after it - and suggest de-risking it early.

## Output format
- Goal and definition of done
- Milestones (3-6)
- Task breakdown per milestone with dependency type (hard/soft)
- Critical path
- Biggest risk/unknown + de-risking suggestion

## Guardrails
Do not fabricate specific time estimates (e.g. "this will take 3 days") unless the user provides their own velocity/capacity data or explicitly asks for a rough guess - state sequencing and dependencies with confidence, but flag duration estimates as guesses when they are.

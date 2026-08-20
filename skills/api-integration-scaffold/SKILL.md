---
name: api-integration-scaffold
description: Given a third-party API's documentation (or URL), produce a typed client wrapper, request/response types, auth handling, error handling, and a test skeleton matched to the project's existing language and conventions. Use when the user needs to integrate a new external API into their codebase.
---

# API Integration Scaffold

## Purpose
Integrating a new API involves the same shape of work every time - auth, typed models, error handling, retries, tests - but hand-rolling it from scratch invites inconsistency with the rest of the codebase. This skill produces a scaffold that matches how the existing project already does things, not a generic template bolted on.

## When to use
The user wants to integrate a new external/third-party API and needs the client code, types, and tests set up.

## Process
1. **Get the API contract.** Use provided docs/URL/OpenAPI spec if available; if not, ask for the specific endpoints needed (method, path, auth scheme, request/response shape) rather than guessing at an API's behavior.
2. **Match existing project conventions**: look at how the codebase already structures API clients (HTTP library used, error handling style, project's typing conventions, test framework) and follow that pattern rather than introducing a new one.
3. **Scaffold the client**: a typed wrapper class/module covering the needed endpoints, with request/response types derived from the actual documented schema (not invented fields).
4. **Handle auth explicitly**: API key/OAuth/token refresh as documented, reading secrets from the project's existing config/env pattern rather than hardcoding them.
5. **Handle errors deliberately**: map documented error responses (rate limits, auth failures, validation errors) to typed exceptions or result types, and note which failures are worth retrying (transient/5xx/rate-limit) versus not (4xx client errors).
6. **Write a test skeleton**: unit tests against mocked responses for the happy path and the documented error cases, plus a note on what an integration/contract test against the real API would need (credentials, sandbox environment) without fabricating one.

## Output format
- Client module/class (typed, matching project conventions)
- Request/response types
- Auth handling
- Error handling with retry guidance
- Test skeleton (mocked happy path + error cases)
- Notes on rate limits/quotas from the documentation, if specified

## Guardrails
Never invent API endpoints, fields, or behavior not present in the provided documentation - ask for the missing piece of documentation instead of guessing. Never hardcode real credentials into scaffolded code or tests; use placeholders wired to the project's existing secret-management pattern.

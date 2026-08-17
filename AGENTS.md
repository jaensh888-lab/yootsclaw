# YOOTS MULTI-AGENT ENGINEERING PROTOCOL v1

Introduced: 2026-08-17. Additive operating standard for humans, ChatGPT/orchestrator, Claude Code, Codex and future Yoots Digital Employees.

## Source of truth
Before non-trivial work read current repository state, local Project OS/current-state/task/decision/risk/deployment docs, tests/CI/runtime evidence, then the current task packet. Chat/model memory is orientation only when it conflicts with GitHub or evidence.

## Roles and routing
- `human:zhanat`: owner/approver.
- `ai:chatgpt-orchestrator`: orientation, decomposition, direct low-risk repo work, Work Packets, review and reconciliation.
- `runtime:claude-code` / `runtime:codex`: coding executors when terminal/browser/build/debugging/large implementation is needed.
- `employee:<id>`: persistent Yoots Digital Employee identity when assigned; employee != runtime/model.

Use orchestrator/direct tools for bounded, verifiable low/medium-risk work. Escalate to a coding runtime when shell, dependency/build/test loops, browser/e2e, complex refactor/debugging or substantial multi-file implementation materially helps. Human approval is required before production deploys, Cloudflare/DNS/routes, secrets/credentials, irreversible migrations/destructive data changes, financial actions, real-client bulk publication/outreach, privileged merges or security-policy relaxation.

## Work Packet
Coding runtimes receive TASK ID, GOAL, BASE branch/SHA, IN-SCOPE, MUST REUSE, MUST NOT/no-touch, acceptance criteria, verification commands/evidence and expected branch/commit/PR + OS/log updates.

## Safety
Existing repository-specific rules remain authoritative; stricter rules win. Do not delete, rename, overwrite, rewrite history, force-push or mass-format unrelated files without explicit scope. Use dedicated branches for non-trivial writes. Do not auto-merge protocol/docs changes: main may trigger CI/CD/Cloudflare. Protocol adoption must not change application code, production, Cloudflare resources, DNS/domains/routes, secrets, migrations, index/noindex behavior or client data. Never store secrets, raw credentials, private chain-of-thought, unnecessary PII or sensitive client payloads in Git/logs.

## Verification and daily ledger
Executor != automatic verifier. Independently inspect actual diff, scope, acceptance criteria, tests/build/CI, regressions, secrets/PII and production claims; record PASS / PASS WITH FOLLOW-UPS / FAIL-BLOCKED.

Every meaningful workday gets a ledger. Reuse existing local daily memory/OS when appropriate; otherwise use `docs/operations/DAILY/YYYY-MM-DD.md`. Separate `ACTION`, `FACT`, `DECISION`, `STATE CHANGE`; record actors, task ID, branch/base SHA/commit/PR, tests/evidence, blockers and exact next action. Daily history does not replace current-state/task/decision/release records.

Completion: `Task ID -> branch -> commit(s) -> tests/evidence -> PR/result -> independent review -> Project OS reconciliation -> exact next action`.

If instructions conflict or state is uncertain, preserve existing state, stop consequential action, document conflict and escalate.
# BATCH-152 — Compiler Extract

## Scope
Compiler- and runtime-facing implications extracted from the agent-bridge source.

## High-Value Compiler Claims
1. Agent intent can be translated into bounded execution primitives against a scoped workspace.
2. The main runtime routes are:
   - `/ide` for browser IDE reverse proxying
   - `/api/exec` for bounded command execution
3. A viable bridge contract includes:
   - command whitelist
   - workspace scoping
   - auth gate
   - audit logging
   - rollback strategy
4. The system should distinguish between:
   - local/prod Docker-backed runtime
   - cloud-preview direct-process runtime
5. Future richer action layers may replace raw shell-only execution with JSON-RPC style actions such as `saveFile` and `readFile`.

## Likely Compiler Audit Targets
Agent intent to execution primitive mapping.
Command whitelist structure.
Workspace scoping enforcement.
Runtime mode switching logic.
Migration path from shell proxy to richer action API.
Audit logging and rollback contract.

## Risk Surface
Any architecture that assumes the same runtime environment across Bolt preview and local/prod hosting would overstate feasibility.
Any agent-facing bridge without whitelists, scoping, logging, and rollback would underuse the strongest safety signals in this batch.

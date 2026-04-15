# BATCH-199 — Compiler / Runtime Extract

## Scope
This extract captures the strongest compiler/runtime material from the branch summary.

## Source-Backed Points
- Input/output contract:
  - Sleeve JSON -> RuntimeSpec + Trace
- Deterministic pipeline:
  - parse
  - validate
  - choose snap
  - select snap blocks
  - remove Off blocks
  - resolve stacks
  - apply triggers
  - enforce authority/directionality
  - merge
  - validate PrimaryShell
  - emit RuntimeSpec
  - emit Trace
- Same-type stack resolution is keyed by `(molt_type + stack_key)`, highest stack_rank wins, deterministic tiebreak by block_id.
- Trigger v0 is actions-only and cannot:
  - rewrite content
  - reorder hierarchy
  - bypass trace
  - change PrimaryShell meaning
  - evaluate conditions
- Merge is same-type only, requires shared non-empty merge_key, and supports explicit policy choices.
- dev/prod conflict behaviors are distinguished.
- Trace event integrity and RuntimeSpec/Trace consistency are mandatory.

## Compiler / Runtime Pressure
This batch strongly pressures the project toward:
- immediate compiler scaffold and tests
- canonical Trace event definitions
- exact stack and merge enforcement
- authority and directionality checks at compile time
- strict execution neutrality of RuntimeSpec

## Conservative Intake Reading
Useful for:
- compiler implementation planning
- audit log seeds
- deterministic behavior requirements
- trace compliance rules

Not enough to:
- settle every UI mechanic around scopes/snaps
- settle all future backend/provider integrations
- replace primary-source implementation docs

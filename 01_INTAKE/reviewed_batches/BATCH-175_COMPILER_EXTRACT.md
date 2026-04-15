# BATCH-175 — Compiler Extract

## Compiler-Relevant Evidence
This file isolates compiler-facing signals from the batch.

## Proposed Input / Output Contract
- **Input:** Sleeve JSON
- **Output:** RuntimeSpec + Trace

## Proposed v0 Pipeline
1. parse
2. validate
3. choose snap
4. select snap blocks
5. remove Off blocks
6. resolve stacks
7. apply triggers
8. enforce authority / directionality
9. merge
10. validate PrimaryShell
11. emit RuntimeSpec
12. emit Trace

## Stack Logic
- Same-type only
- Keyed by `(molt_type + stack_key)`
- Highest `stack_rank` wins
- Deterministic tiebreak by `block_id`

## Trigger Logic
Allowed v0 actions repeatedly proposed as:
- enable_blocks
- disable_blocks
- set_directive_params
- request_tool
- set_merge_mode

Explicitly disallowed:
- rewriting block content
- reordering hierarchy
- bypassing trace
- evaluating conditions in v0
- changing PrimaryShell meaning

## Merge Logic
Eligibility:
- same MOLT type
- same non-empty `merge_key`

Policies mentioned:
- strict
- append
- dedupe_append
- compose_fields (strict in v0 framing)
- prefer_higher_rank

Conflict behavior:
- dev mode: deterministic winner + warning + trace record
- prod mode: explicit compile failure + trace conflict record

## Compiler Risks / Open Items
- Terminology collision around `stack`
- Snap semantics need crisp compiler-facing definition
- RuntimeSpec schema still needs hard formalization
- Trace event taxonomy needs canonical enumeration and tests

## Stage 1 Disposition
Forward to compiler audit/spec drafting as evidence only.

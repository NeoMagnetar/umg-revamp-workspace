# BATCH-015 — Compiler Extract

## Scope
Compiler/runtime implications surfaced by the batch.

## Main Findings
- Request interpretation remains: parse MOLT skeleton -> determine relevant stacks -> apply governance -> select blueprint -> emit output -> optional reflect/polish.
- Runtime self-improvement and bounded agency remain governed by typed contracts, anti-thrash locks, drift thresholds, governance lock, and audit trace requirements.
- Output-envelope rules should not be treated as control authority inside compiler/runtime design.
- Active Stack visibility is a runtime reporting contract candidate.

## Candidate Tasks
- Implement/request-flow validation for layer placement:
  - governance upstream
  - project/runtime posture visible
  - blueprint/output downstream
- Implement runtime trace/report surfaces that distinguish active state from available-but-inactive state.
- Preserve blueprint/output selection as orthogonal to reasoning/stack selection.
- Support host-specific deployment profiles without changing semantic layer order.

## Constraints
- no governance mutation
- no semantic drift caused by packaging
- no collapse of preferences into control logic
- no silent envelope-driven state mutation

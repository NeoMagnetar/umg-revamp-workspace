# BATCH-157 — Compiler / Runtime Extract

## Runtime-Oriented Findings
- UMG is proposed to route ARC-like or grid-logic tasks selectively to `hrm.solver`.
- UMG verifier logic is proposed to inspect confidence, halting behavior, and output quality after solver execution.
- If confidence is low, UMG may trigger another bounded refinement burst rather than unlimited retries.
- Majority vote, self-consistency, loop budgets, and solver selection are treated as runtime control functions at the UMG layer.

## Candidate Runtime Tasks
- define a wrapped-solver invocation contract
- define confidence-gated retry behavior
- define fallback behavior when specialist solver confidence is low
- define standardized trace outputs for halt decisions, loop counts, and vote tallies
- define how solver-internal voting interacts with UMG-level verification

## Candidate Compiler / Audit Tasks
- add metadata support for specialist solver modules
- add runtime trace surface for wrapper-level explainability
- normalize invocation pathway for Python / WSL-backed modules
- preserve auditability around latent solver execution rather than relying on solver internals alone

## Key Open Questions
- Should HRM remain a wrapped external runtime only, or should UMG semantics eventually mirror its planner / worker split?
- How much verification should remain internal to the specialist solver vs externalized to UMG?
- What canonical abstraction should represent specialist wrapped modules?

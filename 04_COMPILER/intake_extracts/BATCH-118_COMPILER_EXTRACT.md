# BATCH-118_COMPILER_EXTRACT

## Compiler / Runtime-Relevant Signal
- Determinism claims must be scoped to specification-layer resolution only.
- UMG should be described as compiling to constraints or cognitive artifacts, not to behavior.
- Near-runtime structural mutation is a claimed strength, but requires formal diff and decision-trace semantics.
- Review pressure requires explicit tie-breaking and fail-closed behavior under unresolved conflicts.
- Governance contract details remain underspecified and need formal operational boundaries.

## Candidate Compiler Tasks
- Define deterministic resolution semantics under identical inputs.
- Define exact tie-breaking and fail-closed behavior.
- Add mutation diff / decision trace semantics for governed structural updates.
- Define governance contract:
  - allowed operations
  - forbidden operations
  - OFF participation semantics
- Keep runtime stochasticity out of specification-layer novelty claims.

## Risk Notes
- Token reduction is plausible but unmeasured.
- Training-use claims risk being misread as training-algorithm novelty.
- Mutation claims risk collapsing into prompt-editing language unless formally separated.

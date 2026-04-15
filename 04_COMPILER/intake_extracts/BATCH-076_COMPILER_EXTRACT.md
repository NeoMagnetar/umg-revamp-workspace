# BATCH-076_COMPILER_EXTRACT

## Scope
Compiler/runtime-adjacent material only.

## Extracted Signals
- UMG is described as a compiler for structured prompts.
- Runtime is framed as ActiveStack + MOLT Map execution.
- The implied flow is:
  1. Invocation
  2. Stack load
  3. Output render
- Governance is treated as precedence logic that constrains later execution.
- “Structure reconstructs from grammar” implies a transferable representation layer across sessions or models.
- Slash-based invocation is proposed as an activation mechanism.
- Workspace files and continuity artifacts act as persistence or reload surfaces.

## Candidate Compiler Impacts
- explicit invocation parsing
- stack-load semantics
- governance precedence law
- merge-direction formalization
- runtime reconstruction from structured grammar
- cross-model portability contract

## Open Compiler Questions
- What exactly is loaded at invocation: sleeve, stack, governance block, or all three?
- How are merge-direction rules enforced?
- Is governance a compile-time validation layer, runtime constraint layer, or both?
- What formal data shape corresponds to ActiveStack and MOLT Map at execution time?

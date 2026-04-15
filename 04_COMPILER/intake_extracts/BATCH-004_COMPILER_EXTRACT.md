# BATCH-004 — Compiler Extract
## Compiler-Relevant Signals
- Enforce one Primary per stack at compile time.
- Allow layered Instructions without violating stack identity.
- Treat bundles as policy-bearing runtime groupings rather than simple labels.
- Validate required CTX fields before execution.
- Assert governance anchor presence before runtime flow begins.
- Preserve MODE vs BP_MODE separation in compiler output contracts.
- Validate self-improvement admissibility rules and prohibit governance mutation.

## Candidate Compiler Tasks
- Compile-time validation for Primary uniqueness and Instruction layering.
- Bundle-policy enforcement hooks for candidate generation, alignment/risk gating, anti-thrash locking, and self-improvement rules.
- Contract validation for typed runtime outputs.
- Governance immutability enforcement across runtime modification paths.

## Compiler Caution
This batch contains implementation-grade ideas, but the referenced runtime material remains draft-level evidence rather than locked canonical contract.

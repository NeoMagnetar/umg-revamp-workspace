# BATCH-127 — Compiler Extract

## Scope
Compiler-facing implementation and release implications extracted from the source.

## High-Value Compiler Claims
1. The compiler is a standalone implementation artifact distinct from the UMG specification repo.
2. The compiler transforms authored structures into RuntimeSpec plus Trace.
3. The compiler is intentionally headless and non-executing.
4. `compileSleeve` is the main public entrypoint.
5. CLI behavior should remain a thin adapter around compiler logic.
6. TriggerState is part of the input model, including bundle-style input patterns.
7. Priority, merge, governance, and ordering are treated as explicit compiler responsibilities.
8. Trace should explain structural decisions rather than leaving them implicit.
9. Package surfaces such as `bin`, `exports`, `main`, `types`, and `files` matter for the compiler’s trustworthiness and reuse.
10. Exit codes, deterministic build flow, and golden-path verification matter for automation and downstream use.

## Likely Compiler Audit Targets
Public API stability around `compileSleeve`.
CLI and library parity.
Trace completeness for priority, merge, and governance decisions.
Deterministic input-output verification.
Packaging and export surface stability.
Separation between compiler core logic and transport/UI/runtime layers.

## Risk Surface
Any drift that re-entangles compiler logic with Studio or UI concerns would conflict with this batch.
Any implementation that adds inference, model calls, or hidden runtime behavior to the compiler surface would conflict.
Any future release process that blurs spec and implementation authority would reduce the clarity this batch established.

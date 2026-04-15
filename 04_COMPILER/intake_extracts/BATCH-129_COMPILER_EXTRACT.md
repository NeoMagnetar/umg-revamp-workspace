# BATCH-129 — Compiler Extract

## Scope
Compiler-facing implications and candidate tasks extracted from the source.

## High-Value Compiler Claims
1. UMG should remain a deterministic specification and compilation layer rather than an execution runtime.
2. RuntimeSpec plus Trace remain the key downstream artifacts.
3. Governance should remain the only legitimate override mechanism.
4. Formal semantics for Merge, Governance, and deterministic synthesis still need publication.
5. Compiler rigor depends on conformance tests and a published Trace schema.
6. A future Trace-of-Selection could extend traceability for candidate generation and selection loops.
7. Hard-gate validation should deterministically reject illegal states before any softer scoring logic is applied.
8. Runtime adapters are a future dependency for turning UMG into interoperable infrastructure.

## Likely Compiler Audit Targets
Formal Merge semantics.
Formal Governance semantics.
Deterministic synthesis rules.
Trace schema publication.
Conformance testing.
Possible hard-gate / soft-score boundary design.
Trace-of-Selection feasibility and audit requirements.

## Risk Surface
Any future extension that lets an LLM bypass structural validity or governance would conflict with this batch.
Any presentation of exploratory rescoring as already-canonical compiler behavior would overstate the source.
Any collapse of specification, compilation, and execution into one layer would conflict with the boundary language preserved here.

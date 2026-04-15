# BATCH-110 — Compiler Extract

## Compiler-Relevant Signal
This batch contributes terminology discipline and artifact-boundary language more than new algorithmic behavior, but that language is important for compiler/spec alignment.

## Stable Compiler-Relevant Points
- UMG specifies cognition prior to execution.
- Compilation transforms resolved cognition into an execution-facing representation and **does not add meaning**.
- Deterministic resolution is a non-negotiable invariant.
- Governance must apply before lower-level resolution behavior.
- Audit traceability is required.
- Runtime-facing artifacts should remain distinct from specification artifacts.
- Agents / executors consume constrained artifacts rather than authoring cognition.

## Candidate Compiler Tasks
- Define CIR explicitly as the compiled output of resolved cognitive specifications.
- Formalize decision trace generation.
- Enforce governance-before-resolution ordering.
- Preserve semantic equivalence through terminology translation layers.
- Separate:
  - canon semantics,
  - mapping labels,
  - proof language,
  - executor-facing artifacts.

## Terminology Sensitivity
This batch increases pressure to keep wording precise:
- Do not let external terminology translation imply semantic drift.
- Do not let formal proof language silently introduce canon beyond what the project explicitly approved.
- Keep unresolved items labeled as unresolved in compiler-adjacent documentation.

## Migration / Audit Pressure
Compiler-adjacent docs and code comments should be checked for:
- wording that implies execution invents meaning
- wording that weakens governance ordering
- wording that conflates mapping language with canon rules
- wording that fails to preserve auditability and determinism guarantees

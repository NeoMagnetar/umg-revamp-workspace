# BATCH-109 — Compiler Extract

## Compiler-Sensitive Findings
- Reject all descriptions that make CSL a compiler input or compilation source.
- Preserve a strict separation between:
  - **admissibility/jurisdiction** under CSL
  - **resolution/binding** by UMG
  - **execution enforcement** by PCL / Executor

## Stabilized Compiler/Runtime Boundary
1. Governance may enable/disable cognition before lower-level processing.
2. CSL defines admissible cognitive space.
3. UMG resolves and binds admissible cognition.
4. CIR is instantiated/validated within CSL jurisdiction.
5. RuntimeSpec is the executor-facing resolved envelope.
6. Trace is emitted as the audit artifact.
7. PCL loads RuntimeSpec and constrains execution.
8. Executor performs reasoning/action within the bounded envelope.

## Language to Remove
- “CSL compiles into CIR”
- “CSL emits CIR”
- “CSL produces runtime artifacts”
- “CSL is a language” when jurisdiction/layer meaning is intended

## Safer Replacement Language
- “CIR is instantiated and validated within CSL.”
- “UMG Compiler is a pre-runtime resolution and binding engine.”
- “RuntimeSpec is the executor-facing result of UMG-level resolution.”
- “Trace records the resolution outcome and authority path.”

## Candidate Compiler Tasks
- Audit all docs/specs for “CSL → CIR” leakage.
- Rename any compiler-stage descriptions that incorrectly list CSL as an input artifact.
- Standardize “resolution/binding” wording wherever “compilation” was used loosely.
- Preserve separate spec sections for:
  - admissibility
  - resolution
  - runtime enforcement
  - audit

## Risk Note
Retaining the term “UMG Compiler” is acceptable only if compiler behavior is explicitly attached to UMG-level pre-runtime resolution rather than to CSL.

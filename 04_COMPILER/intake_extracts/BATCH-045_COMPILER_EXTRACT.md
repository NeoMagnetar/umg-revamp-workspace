# BATCH-045 — Compiler Extract

## Compiler-Relevant Signals
- Normalize runtime explanation so diagrams and compiler-facing language use the same flow:
  - request -> sleeve -> stack activation -> NeoBlock compilation -> MOLT assembly -> emission
- Avoid visual semantics that imply governance is a mutable sleeve subcomponent.
- Align compiler-oriented explanation of NeoBlocks with **compiled activation/projection view** semantics.

## Candidate Compiler Tasks
- Standardize diagram/runtime wording for activation and compilation phases.
- Audit current explanatory materials for contradictions between containment language and projection/compiled-view language.
- Preserve separate public and canonical diagram tracks so simplified artifacts do not silently overwrite compiler-accurate architecture.

## Risk Notes
- Public compression can accidentally imply wrong execution semantics.
- Governance placement errors can weaken claims of invariance and deterministic control.

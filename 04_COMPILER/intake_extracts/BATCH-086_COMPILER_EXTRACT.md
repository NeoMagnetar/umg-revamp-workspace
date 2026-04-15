# BATCH-086 — Compiler / Runtime Extract

## Scope
This extract captures the compiler/runtime-adjacent surfaces that appear in the batch.

## Source-Backed Points
- Merge blocks combine supporting logic into the Primary directive.
- Merge logic determines how auxiliary data is injected into output.
- Runtime is broadly described as:
  - Primary defines objective
  - Merge injects required details
  - Blueprint shapes presentation
- UMG engine is described as merging blocks into final prompt/output.
- Candidate implementation tasks include:
  - block merge engine for prompt construction
  - provenance tracking through NeoCPF

## Compiler / Runtime Pressure
The batch suggests that provenance should not remain purely documentary. It pressures the project toward:
- origin tracking at block level
- versioned block histories
- authorship-aware runtime/logging
- merge surfaces that can later emit provenance metadata

## Conservative Intake Reading
Useful for:
- compiler audit seeds
- provenance hook planning
- merge-engine task extraction

Not enough to:
- settle final merge law
- define execution priority
- define trigger semantics
- define finalized NeoCPF runtime schema

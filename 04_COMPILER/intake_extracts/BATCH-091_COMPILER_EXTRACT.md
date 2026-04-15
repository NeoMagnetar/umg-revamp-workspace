# BATCH-091 — Compiler / Runtime Extract

## Scope
This extract captures the strongest compiler/runtime surfaces preserved in the consolidation batch.

## Source-Backed Points
- Priority system is numeric:
  - 0 = off
  - 1 = primary
  - 2 = secondary
  - 3 = tertiary
- Priority affects execution order and token weighting.
- Merge engine handles hierarchy and prompt-stack construction.
- UMG preamble defines interpretation rules for API execution.
- Runtime pipeline includes:
  - input parsed
  - context map generated
  - MOLT-driven response rendered
  - reflection injected
- Token weighting affects resource allocation.
- Commando-style implementation references indicate:
  - merge engine
  - token calculator
  - UI scaffolding
  - presets/loadouts

## Compiler / Runtime Pressure
This batch reinforces the need to formalize:
- merge-engine behavior
- token weighting semantics
- interaction between semantic priority and numeric weighting
- reflection injection boundaries
- block conflict resolution

## Conservative Intake Reading
Useful for:
- compiler audit notes
- execution-model normalization
- merge and priority task extraction

Not enough to:
- settle final merge conflict law
- settle exact meta-layer override authority
- settle complete execution semantics across all artifacts

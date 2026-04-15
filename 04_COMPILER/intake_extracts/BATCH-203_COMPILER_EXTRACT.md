# BATCH-203 — Compiler / Runtime Extract

## Scope
This extract captures loader and runtime-activation implications from the architecture summary.

## Source-Backed Points
- Runtime is defined as selective loading of sleeves and blocks into chat/agent execution surfaces.
- Loader behavior is conceptually import-like:
  - explicit object ID loading
  - no assumptions about undeclared modules
  - mark missing definitions rather than invent them
- A three-pass canonization workflow is proposed:
  - inventory pass
  - normalization pass
  - backlog generation
- External canon plus selective loading implies dependency resolution and object lookup behavior.

## Compiler / Runtime Pressure
This batch strongly pressures the project toward:
- explicit loader contract
- dependency resolution by object ID
- duplicate and missing object validation
- strong separation between static canon and active runtime state
- clear import/projection semantics for sleeves, blocks, and stacks

## Conservative Intake Reading
Useful for:
- loader planning
- canon/runtime boundary docs
- dependency and validation design

Not enough to:
- settle final schema fields
- settle final loader syntax
- settle final NeoStack loading law

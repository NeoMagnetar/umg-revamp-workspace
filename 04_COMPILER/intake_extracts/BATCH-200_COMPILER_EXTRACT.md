# BATCH-200 — Compiler / Runtime Extract

## Scope
This extract captures orchestration and prompt/runtime implications from the repo-evaluation summary.

## Source-Backed Points
- A Citadel Core / Orchestrator is inferred as the coordinator for:
  - collecting Primary output
  - merging auxiliary context
  - applying Blueprint shaping
  - building final prompt
  - submitting to the model
  - optionally parsing/displaying/exporting result
- Prompt assembly is identified as a central runtime function and possible site of duplication.
- Registry/config-driven definitions for block types and capabilities are proposed.
- Logging/traces are recommended so each block reports what it did during execution.

## Compiler / Runtime Pressure
This batch pressures the project toward:
- centralized prompt construction/orchestration
- explicit block-interface or registry model
- architecture-aware tooling interfaces
- observable execution traces for each block or capability call

## Conservative Intake Reading
Useful for:
- orchestrator design ideas
- runtime visibility requirements
- centralized prompt-assembly cleanup

Not enough to:
- prove actual repository implementation details
- settle final capability-execution model
- settle exact block base-class architecture

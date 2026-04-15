# BATCH-084 — Definitions Extract

## Terminology
### UMG Preamble
Runtime framing that states the system interprets logic through a hierarchy of blocks with priority and token weighting.

### Reality Core
Product/app framing for the broader UMG framework runtime platform.

### Mind HUD
Transparency/UI layer sitting above runtime and formatting surfaces.

### MemoryCore (MEC)
Memory layer referenced as part of runtime system composition.

## Role Language
### Primary
Main runtime directive or task scope.

### Subject
Domain/context focus for the execution.

### Philosophy
Alignment/utility lens and self-check posture.

### Instruction
Execution behavior such as merge priority, recursive execution, checklists, fallback, or status controls.

### Merge
Task-layer compilation or block fusion surface used to form executable payloads.

## Runtime / Compiler Language
### CompileMOLT
Validation + normalization + fallback injection stage for block input.

### mergeBlocks
Function that filters priority-zero blocks, sorts remaining blocks by priority, and compiles a structured payload.

### mergeBlocksToTask
Task-oriented merge function that compiles blocks into payload + steps and derives a task type.

### assembleUMGPayload
Runtime function that combines preamble plus merged blocks into final executable prompt payload.

### callLLM
Unified adapter surface for routing payloads to model backends.

### routeStrategy.json
Control file mapping task/model roles and fallback routing.

### privacyModes.json
Control file defining privacy behavior modes such as off, audit-only, and strict.

## Definitional Candidates
- CompileMOLT = validator/normalizer with fallback injection
- mergeBlocksToTask = compiler surface converting block stacks into executable task payloads
- UMG runtime = parser -> compiler -> route -> validate -> execute -> format -> HUD

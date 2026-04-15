# BATCH-158 — Blocks / MOLT Extract

## MOLT / Planning Signals
- MOLT is mapped to plan synthesis.
- PlanNode intents include:
  - gather
  - transform
  - decide
  - act
  - verify
- Preferred loop shape:
  - decide → act → verify

## Trigger Signals
Explicit scaffolded triggers include:
- ON.USER_CMD:SAVE.POE -> STORE+SYNC.VLT
- ON.MEMORY.DUMP -> CHECK+PRUNE+REWRITE

## Block-Like Runtime Units
The source composes modular runtime units that behave like blocks/config units:
- alignment block
- mythos block
- trigger blocks
- overlay blocks
- instruction layer
- philosophy stack

## Checklist / Mutation Discipline
The scaffold includes:
- UNDERSTAND > REFLECT > REFINE
- MUTATION: ONLY_IF(SUPERIOR)
- MEMORY_DUMP: TRIGGER > REWRITE.IF.GAIN > THRESHOLD

## Stage 1 Note
These terms and mappings are strong evidence for planning/runtime structuring, but not stable canon yet.

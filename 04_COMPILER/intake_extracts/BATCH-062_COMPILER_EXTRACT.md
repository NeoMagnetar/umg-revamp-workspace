# BATCH-062 Compiler Extract

## Observed Runtime Candidates
- runtime loading order: vault -> alignment -> overlay
- checklist logic: understand -> reflect -> refine
- trigger handling for:
  - SAVE.POE / store + sync
  - MEMORY.DUMP / check + prune + rewrite
  - REDUCE commands
- controlled mutation via authorized, traceable vault merges
- memory sweep preserving core stack and essential overlays
- portable export / restoration spine

## Potential Compiler / Runtime Tasks
1. Formalize aligned boot-chain load order.
2. Define explicit trigger schema for save, reduce, and memory-dump events.
3. Define controlled-mutation merge rules and superiority criteria.
4. Define memory sweep semantics:
   - what is preserved
   - what is pruned
   - what requires reconfirmation
5. Define export/import format for portable core restoration.
6. Clarify when CantoCore is descriptive syntax versus executable runtime syntax.

## Confidence / Status
Evidence only. The batch supports a concrete runtime direction and vocabulary, but not a finalized implementation spec.

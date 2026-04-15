# BATCH-013_COMPILER_EXTRACT

## Scope
Compiler/runtime implications from the batch.

## Extracted Compiler Signals
- Validate `STACK_CONTROL` and `SLEEVE_CONTROL` as staged intents, not immediate mutations.
- Apply approved changes on the next turn only.
- Maintain runtime registries:
  - `STACK_REGISTRY`
  - `NEOBLOCK_REGISTRY`
  - `DELTA_LOG`
- Enforce:
  - no governance mutation
  - no enabling project-`OFF` stacks
  - no silent persistence to canon
- Validate runtime-created:
  - Blocks
  - NeoBlocks
  - NeoStacks
  - merges
  - bundles

## Bounded Runtime Mutation
Allowed only when:
- policy permits,
- governance remains unchanged,
- target stack is `ON` or `ADAPTIVE` as appropriate,
- result stays session-local unless explicitly promoted.

## Candidate Tasks
- lock/dependency checking for stack and sleeve control
- next-turn application queue
- registry-backed snapshot emission
- validation for runtime-created structures
- renderer/presentation errors classified without implying state exit

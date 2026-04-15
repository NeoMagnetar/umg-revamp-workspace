# BATCH-042 — Compiler Extract

## Compiler-Relevant Signal
This batch implies a deterministic sleeve activation contract rather than a loose prompt-mode switch.

## Candidate Runtime Flow
1. receive sleeve / mode selection
2. resolve selected sleeve ID
3. load sleeve profile
4. enumerate NeoStacks
5. generate primary NeoBlock per NeoStack
6. generate instruction NeoBlocks
7. optionally attach bundles
8. emit full sleeve structure in first response
9. persist selected sleeve until explicit switch

## Candidate Compiler Tasks
- implement first-response auto-expansion from selected sleeve into:
  - NeoStacks
  - Primary NeoBlocks
  - Instruction NeoBlocks
  - Optional Bundles
- support persistent in-sleeve state until explicit switch
- normalize names and IDs across the 60-sleeve catalog
- run stack reuse analysis across the catalog
- prepare later compatibility / conflict / merge matrix support

## Implementation Notes
- This batch is strong at sleeve and NeoStack level.
- NeoBlock detail remains pending / on-demand rather than fully authored.
- Activation doctrine is stronger than low-level compiled detail and should be treated as protocol evidence.

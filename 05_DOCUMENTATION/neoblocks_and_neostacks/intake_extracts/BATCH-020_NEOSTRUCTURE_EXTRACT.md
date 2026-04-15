# BATCH-020 — NeoStructure Extract

## NeoStack / NeoBlock Placement
This batch does not redefine NeoStructure theory, but it does make NeoBlocks and NeoStacks first-class stored and managed components inside the homebase repo.

## Strongest Structural Signals
- NeoBlocks should live under `blocks/neoblocks/`
- NeoStacks should live under `blocks/neostacks/`
- active stack should be tracked explicitly in runtime control files
- compiler-aware flows should keep source structures separate from live runtime state

## Applied Pattern
The homebase repo becomes a management surface where:
- source NeoBlocks / NeoStacks are stored
- selected runtime posture is made explicit
- compiler outputs are derived into separate runtime paths

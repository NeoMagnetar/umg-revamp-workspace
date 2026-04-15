# BATCH-020 — Blocks / MOLT Extract

## Asset Taxonomy Signal
The batch repeatedly separates stored asset classes rather than collapsing them into one folder or one file.

## Strongest Asset Classes
- `blocks/molt/`
- `blocks/neoblocks/`
- `blocks/neostacks/`
- `blocks/manifests/`

## Working Implications
- MOLT blocks remain a distinct stored source layer
- NeoBlocks remain distinct from MOLT blocks
- NeoStacks remain distinct from both
- manifests can mediate relationships between asset layers

## Structural Rule Candidates
- keep asset classes separate
- do not treat compiled runtime state as source truth
- do not silently overwrite user-provided canonical files

# BATCH-165 Canon Candidates

## Candidate Language
- “The builder is manifest-driven: selected plan → manifest → block IDs → individual block loads → canvas/graph render.”
- “Block integrity must be explicit: duplicate IDs, invalid edges, and failed loads should throw visible errors rather than silently degrade.”
- “The UMG builder separates data/model layers from rendering layers.”

## Candidate Documentation Targets
- builder data layout
- plan-manifest-to-block-load pipeline
- failure classes for builder runtime
- Bolt-export-to-GitHub replacement workflow

## Candidate PRD Targets
- visible failure over silent degradation
- graph navigation affordances
- multi-pane editor behavior
- validation pipeline before release

## Evidence Warning
These are candidate formulations derived from implementation discussion. They should not be promoted without comparison against other builder batches and live repo evidence.

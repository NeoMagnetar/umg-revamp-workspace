# BATCH-006 — Blocks and MOLT Extract
## Blocks / MOLT Signals
- MOLT is treated as an authority model, not just a lane-ordering grammar.
- The batch sharply distinguishes:
  - authority precedence
  - prompt assembly order
  - display/rank order
- Trigger blocks currently behave too descriptively in the compiler example; the intended direction is true branch/runtime activation.
- Bundles are treated as the natural home for ranked groups, alternates, exclusivity, and conditional activation.
- NeoBlocks should eventually reflect resolved active truth rather than raw pre-resolution inclusion.

## Candidate MOLT / Block Tasks
- Lock the canonical authority-precedence contract.
- Define trigger execution semantics relative to bundles, alternates, and directive switching.
- Clarify when in-lane ranking matters versus when authority or conditions dominate.
- Clarify how bundles represent mutually exclusive winners and conditional branches.
- Preserve bundle/merge distinctions without widening schema churn unnecessarily.

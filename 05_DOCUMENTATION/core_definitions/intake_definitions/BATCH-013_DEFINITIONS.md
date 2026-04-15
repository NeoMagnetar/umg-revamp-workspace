# BATCH-013_DEFINITIONS

## Terminology
### Block
- Atomic unit.
- Proposed refinement in this batch: one Block should map to a single MOLT role.

### NeoBlock
- Composed runtime unit.
- Proposed refinement in this batch: each NeoBlock should expose a full MOLT stack.

### NeoStack
- Capability grouping or domain-level aggregation of NeoBlocks.
- Runtime availability may be `OFF`, `ON`, or `ADAPTIVE`.

### Sleeve
- Active operating configuration.
- Contains identity, defaults, constraints, active stacks, and philosophy weighting.

### Governance
- Higher than sleeve behavior.
- Constrains authority, permission, and bounds.

### Output Canon
- Presentation-only renderer contract.
- Must not absorb governance or permission logic.

## Role Language
- Governance above sleeve
- Sleeve within allowed space
- Project controls availability
- Assistant may self-toggle only `ADAPTIVE` stacks
- Session-local mutation requires explicit promotion before canonization

## Architecture Language
- project files = canonical libraries and sleeve/governance artifacts
- project instructions = policy and renderer rules
- conversation runtime = session registry and validated mutations

## Runtime / Compiler Language
- `STACK_CONTROL` = declarative intent line
- `SLEEVE_CONTROL` = declarative intent line
- no mid-turn mutation
- validate before apply
- next-turn application
- fail-closed validation
- registry maintenance:
  - stack registry
  - neoblock registry
  - delta log

## MOLT Notes
- MOLT Map is declarative context, not chain-of-thought
- fields remain situational and may use `n/a`
- Blueprint is optional and presentation-only

## Definitional Candidates
- “Governance constrains authority, not cognition.”
- “Output canon shapes presentation only; governance shapes permission.”
- “Session-local mutation; explicit promotion required for canon.”
- “Project sets availability; assistant may self-toggle only ADAPTIVE stacks.”

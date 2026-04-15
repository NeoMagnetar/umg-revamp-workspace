# BATCH-050 — Compiler Extract

## Compiler-Relevant Signals
- Enforce strict ontology:
  - every NeoStack contains NeoBlocks
  - every NeoBlock contains one or more MOLT atoms
- Reject flattening where NeoBlocks are treated as atomic primitives.
- Preserve deterministic ordering via:
  - effective weight
  - axis rank
  - merge rank
  - stable identifier
- Reject style/surface overlays that write intent-bearing fields.
- Reject trigger routing that mutates core identity.
- Preserve frozen CORE identity / highest-rank invariants.
- Support runtime validation for:
  - trigger routing
  - merge determinism
  - mutation policy
  - bounded escalation / decay

## Candidate Compiler Tasks
1. Build validator for three-tier ontology below sleeves.
2. Implement deterministic dominance sort key.
3. Implement overlay write restrictions:
   - STYLE_OVERLAY cannot write Directive/Instruction/Primary.
4. Implement trigger constraints:
   - trigger escalation cannot rewrite CORE identity.
5. Preserve linear MOLT as probable interchange format even if richer execution overlays exist.
6. Add external-governance representation layer above sleeve-governance layer.
7. Add continuity semantics distinguishing warm reconstruction from persistent memory/state.

## Risks
- Spatial+weight hybrid may be powerful but difficult to canonicalize cleanly.
- Priority semantics remain unresolved and could destabilize compiler behavior if left implicit.
- Threat/coercion triggers require more formalization to avoid subjective drift.

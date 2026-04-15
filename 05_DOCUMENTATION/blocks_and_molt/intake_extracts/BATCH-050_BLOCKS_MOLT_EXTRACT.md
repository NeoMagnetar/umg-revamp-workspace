# BATCH-050 — Blocks and MOLT Extract

## Canonical Hierarchy Correction
- Sleeve
- NeoStacks (domain containers)
- NeoBlocks (grouped intent)
- MOLT atoms (atomic primitives)

## NeoBlock Composition Findings
- NeoBlocks are grouped intent, not atomic units.
- A valid NeoBlock contains one or more MOLT atoms.
- Grouping is important for:
  - mutation boundaries
  - domain clarity
  - auditability
  - version control
  - semantic stability

## MOLT Taxonomy Findings
- Canonical roles retained:
  - Trigger
  - Directive
  - Instruction
  - Subject
  - Primary
  - Philosophy
  - Blueprint

## Key Guardrail
- Do not flatten grouped intent into atomic weights or atom-level slots.
- Do not allow surface/style modules to rewrite intent-bearing atomic fields.

## Candidate Documentation Rule
- Preserve three-tier ontology below sleeves; do not collapse NeoBlocks into MOLT atoms in canon docs, validators, or runtime serialization descriptions.

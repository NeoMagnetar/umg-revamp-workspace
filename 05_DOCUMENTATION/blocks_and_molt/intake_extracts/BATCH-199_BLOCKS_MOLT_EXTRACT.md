# BATCH-199 — Blocks / MOLT Extract

## Scope
This extract captures taxonomy locking and role/type separation.

## Canonical MOLT Types
- Trigger
- Directive
- Instruction
- Subject
- Primary
- Philosophy
- Blueprint
- Off

## Key Lock
Merge is not a MOLT type. Merge is an operation.

## Role / Type Separation
### PrimaryShell
Role, not MOLT type.

### MergeContributor
Role participating in compatible merge.

### BlueprintGuide
Role expressing silent style/structure influence.

## Authority Order
Trigger > Directive > Instruction > Subject > Primary > Philosophy > Blueprint > Off

## Stability Notes
This batch is one of the strongest explicit lock surfaces for MOLT ordering, role/type separation, and Merge reclassification.

## Project Relevance
Useful for:
- glossary canon
- compiler behavior normalization
- preventing type/role drift
- aligning docs and implementation around fixed vocabulary

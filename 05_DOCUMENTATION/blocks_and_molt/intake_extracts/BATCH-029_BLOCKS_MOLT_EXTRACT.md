# BATCH-029 — Blocks / MOLT Extract

## Block-Library Findings
- Trigger extensions should be ingested by **type** into the Trigger library.
- Business Trigger Blocks are represented as `TRG.101–TRG.200`.
- Trigger entries should remain grouped by their domain section rather than flattened into an undifferentiated list.

## Structural Rules
- preserve exact IDs
- preserve category placement
- preserve section grouping
- do not renumber
- do not compress
- do not duplicate legacy ranges
- do not cross-assign into Directive / Instruction / Subject / Primary / Philosophy / Blueprint

## MOLT Boundary Signal
- Persona is explicitly not treated as a MOLT role in this batch.
- That distinction matters because it keeps the MOLT family focused on cognition and task structure.

## Candidate Reuse
- Block-ingest workflow for future library expansion
- Documentation rule for typed extensions
- Validation rule for upload handlers inside OpenClaw

## Caution
- The ingest rule is strong but still derived from a summarized source, not from a finalized canonical decision artifact.

# BATCH-054 — Definitions Extract

## Terminology
### UMG Block
A concrete repo-level artifact that should carry name, metadata, role typing, provenance, and later runtime meaning.

### Master Builder Citadel / UMG Block Builder
Working framing for a system that turns a large canonical block inventory into real project artifacts rather than leaving them as abstract prompt fragments.

### Master List
The source-of-truth list of block names and possibly descriptions that a future generator/importer should ingest.

### MOLT Type
A semantic and storage/runtime classification attached to a block. In this batch the discussed set includes:
- Primary
- Subject
- Instruction
- Philosophy
- Blueprint
- Directive
- Trigger
- Merge
- Off
- Deployment

### Ledger
Trace/provenance surface attached to a block. Candidate fields include:
- originator
- verified_by
- created_at
- edit_log

### Minimum Sanity Rule
A candidate validity threshold under which every block should at minimum include:
- block_id
- label
- description
- molt_type
- ledger

## Role Language
- blocks must become real files
- canonical names must be preserved
- placeholder “Auto Block” style outputs are insufficient
- Poecore should later interpret and build from the schema

## Architecture Language
### Snap Config
Runtime-facing structure for stacking/snap compatibility and conflict policy.

### Merge Logic
A structured field set for whether and how blocks combine. Candidate fields include:
- can_merge
- merge_strategy
- merge_origin

### Agent Orchestration
A schema surface implying later use of blocks inside automated or multi-step assembly systems.

### Integration Layer
A block field intended to express downstream system or runtime coupling.

## Runtime / Compiler Language
- importer
- generator
- reclassification script
- audit script
- repo placement
- one-pass generation
- global numbering continuity

## Definitional Candidates
- A valid UMG block is not only a name; it is a named artifact with role typing, provenance, and runtime-facing structure.
- MOLT typing is not merely descriptive; it affects storage, interpretation, and later assembly behavior.

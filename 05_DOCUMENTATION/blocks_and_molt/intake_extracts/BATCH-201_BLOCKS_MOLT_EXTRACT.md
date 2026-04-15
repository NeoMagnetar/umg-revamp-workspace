# BATCH-201 — Blocks / MOLT Extract

## Scope
This extract captures active role folders, questioned role status, and block-file semantics.

## Active MOLT Folders
- Blueprint
- Deployment
- Directive
- Instruction
- Meta
- Off
- Philosophy
- Primary
- Subject
- Trigger

## Questioned Types
### Merge
Listed in schema reference, but questioned as a true canonical MOLT type in runtime logic.

### Deployment
Operationally present in folders, manifests, docs, and autoblocks, but its canonical status is still being tested.

## Block Composition Pressure
- Canonical block unit is the individual `.block.json`.
- Legacy aggregate JSONs are being retired as authoring sources.
- Autoblocks are unpacked into ordinary blocks while preserving metadata.
- Template stacks/manifests reference block IDs rather than acting as block content themselves.

## Project Relevance
Useful for:
- taxonomy cleanup
- schema reconciliation
- block-storage canon
- builder/runtime alignment

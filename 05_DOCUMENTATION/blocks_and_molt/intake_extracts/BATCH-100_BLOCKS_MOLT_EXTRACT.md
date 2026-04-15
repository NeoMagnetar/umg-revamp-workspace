# BATCH-100_BLOCKS_MOLT_EXTRACT

## Scope
MOLT / block-schema / starter-library signals extracted from BATCH-100.

## Schema Signal
The source reports one of the clearest early-release schema excerpts so far:
- `id`
- `type`
- `cantocore`
- `version`
- `inputs`
- `outputs`
- `metadata`

This pressures documentation toward:
- mandatory-versus-optional field separation
- type validation rules
- versioning semantics
- input/output conventions for interoperable block execution

## Enumerated Type Signal
The source explicitly lists these block types:
- Primary
- Subject
- Instruction
- Merge
- Overlay

This is important because Overlay appears here as part of the enumerated first-release type surface rather than only as an informal layer metaphor.

## Starter Library Signal
The batch reports a starter library with named example blocks such as:
- `Alignment.Primer.v1`
- `Philosophy.LoveLogic.v1`
- `Subject.ArtOfWar.v1`

This strengthens three documentation needs:
- naming conventions for release-ready blocks
- starter-library curation rules
- separation between example/demo blocks and canonical core blocks

## Structural Tensions
- the type set is concrete, but may not yet be reconciled with earlier broader role inventories
- Overlay appears as a type here, which may conflict with earlier uses of overlay as a layer or composition relation
- starter blocks are implementation-useful, but not automatically canonical semantics
- the exact relation between `cantocore`, `metadata`, `inputs`, and `outputs` still needs schema-level clarification

## High-Value Documentation Targets
- formalize Block JSON schema v0.1
- define block type vocabulary and scope
- clarify whether Overlay is a role, type, layer, or all three
- document starter-library naming and versioning conventions
- distinguish demo inventory from canon-bearing block inventory

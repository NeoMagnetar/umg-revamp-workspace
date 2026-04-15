# BATCH-105_BLOCKS_MOLT_EXTRACT

## Scope
MOLT / block-role / candidate-block signals extracted from BATCH-105.

## Canonical Block Pressure
The batch repeatedly pressures clarity around block structure, especially these fields:
- `content`
- `merge_logic`
- `ledger`
- `schema_version`

This matters because repository drift appears to be happening at the composition level, not only at the semantic level.

## Core Representation Boundary
The source sharpens a useful distinction:
- **CantoCore** = executable rules/grammar surface
- **CyentCore** = descriptive memory-card representation

This is high-value because it prevents utilities, scripts, and memory representations from being conflated.

## MOLT / mutation signal
MetaMolt / MOLT is referenced as an evolution or mutation surface for block refinement. The packet does not expand role taxonomy, but it does imply that transformations of blocks must still remain schema-valid after mutation.

## Trigger / card-level signal
CyentCore card triggers named in the source:
- `schema_validation`
- `repo_audit`
- `pre_migration_check`

These suggest utility-memory cards can be indexed by operational trigger, even when they are not themselves executable artifacts.

## Boundary Pressure
This batch strongly pressures clarification of:
- whether `merge_logic` is a canonical block field or an extension
- whether `content` array form is mandatory across all blocks
- which fields belong inside executable blocks versus descriptive memory cards
- how mutation/evolution systems preserve schema validity rather than amplifying drift

## High-Value Documentation Targets
- document CantoCore versus CyentCore clearly
- define canonical block-field expectations
- document trigger-bearing CyentCore cards as representation, not execution
- specify how mutation/evolution workflows respect schema rules

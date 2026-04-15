# BATCH-054 — Blocks / MOLT Extract

## Core Finding
This batch treats block identity, MOLT typing, and schema completeness as operational requirements for a real UMG block inventory.

## Discussed MOLT-Type Set
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

## Structural Expectations for a Block
### Identity Layer
- block_id
- label
- description
- category
- tags

### Semantic Layer
- molt_type
- cantocore
- example_block_data

### Composition Layer
- snap_config
- merge_logic
- compatible_types
- conflict_policy
- stack_level
- snap_to

### Provenance / Governance Layer
- ledger
- originator
- verified_by
- created_at
- edit_log

### Runtime / Orchestration Layer
- code_modules
- runtime_behavior_flags
- agent_orchestration
- integration_layer
- future_extensions

### Presentation Layer
- display
- color mapping
- edit features

## Key Distinctions
- A block is not just a name.
- A name without correct schema and provenance is insufficient.
- Full MOLT typing should remain visible even if early imports temporarily default many items to one type.
- Snap/merge/stack expectations remain part of block meaning even before full runtime implementation exists.

## Unresolved Points
- Whether all fields belong in the canonical minimum schema.
- Whether initial imports should type minimally or fully.
- Whether Deployment and Off are permanent block types or implementation/control surfaces.

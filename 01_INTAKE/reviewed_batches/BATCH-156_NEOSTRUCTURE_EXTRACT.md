# BATCH-156 NeoStructure Extract

## NeoStructure-Relevant Pattern
This batch provides a comparatively complete draft of how a NeoBlock-style object may be shaped for authoring, rendering, composition, and future execution.

## Candidate Object Shape
Fields surfaced in the source include:
- `block_id`
- `label`
- `category`
- `description`
- `molt_type`
- `tags`
- `cantocore`
- `snap_config`
- `merge_logic`
- `ledger`
- `display`
- `editable_fields`
- `example_block_data`
- `code_modules`
- `runtime_behavior_flags`
- `integration_layer`
- `agent_orchestration`
- `future_extensions`

A simplified documentation-facing variant retained:
- `block_id`
- `label`
- `category`
- `description`
- `molt_type`
- `tags`
- `cantocore`
- `snap_config`
- `merge_logic`
- `ledger`
- `display`
- `code_modules`

## Structural Model
The batch implies a layered NeoStructure:
1. semantic identity
2. composition metadata
3. governance/safety metadata
4. display metadata
5. editability metadata
6. runtime metadata
7. implementation module references
8. future extension space

## Composition Flow
The batch describes:
- snap detection
- provisional stack creation
- merge engine resolution
- sleeve/runtime packaging

This is structurally useful because it maps object shape to assembly workflow.

## Why it matters
This is one of the clearer evidence batches for thinking about NeoBlock design as:
- machine-readable
- human-editable
- UI-renderable
- compiler-attachable
- potentially runtime-deployable

## Cautions
- This is still a draft schema, not stabilized canon.
- A fuller schema and a simplified README schema both appeared.
- The object boundaries between semantics, display, and execution are improved here but still not formally fixed.

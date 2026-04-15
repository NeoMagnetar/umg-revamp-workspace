# BATCH-107 — Blocks / MOLT Extract

## Active Working `molt_type` Set in This Batch
- Primary
- Subject
- Instruction
- Directive
- Philosophy
- Blueprint
- Merge
- Trigger
- CodeBlock
- Off

## Key MOLT Clarifications
- MOLT remains the runtime/semantic role system.
- Category/subcategory/domain remain browsing and library-organization surfaces.
- Browsing taxonomy must not replace MOLT runtime semantics.
- `Trigger` is a semantic role and is not equivalent to executable code payload.
- `CodeBlock` is used when the primary payload is code/markup.
- `Deployment` is legacy/problematic and should not remain a main MOLT type without explicit control-room approval.

## Block Composition Pressure
- Blocks require both semantic and organizational identity.
- Strong required metadata cluster:
  - `block_id`
  - `label`
  - `category`
  - `subcategory`
  - `molt_type`
  - `cantocore`
  - `description`
  - `tags`
  - `display`
  - `code_modules`
  - `snap_config`
  - `merge_behavior`
  - `editable_fields`
- Content shape pressure:
  - `prompt_template`
  - or `body`

## Merge / Snap Signal
- `merge_behavior` is core schema, not optional ornament.
- `snap_config.priority` and `merge_behavior.priority` are normalized runtime-ordering surfaces.
- Builder is expected to snap and merge blocks by MOLT plus runtime metadata.

## Builder Implication
The batch strongly supports this distinction:
- **browse by** domain/category/subcategory
- **snap and merge by** MOLT role plus snap/merge metadata

## Migration Pressure
- remove legacy keys not accepted by strict schema
- normalize legacy content fields
- normalize code module structure
- remove or transform pseudo-roles that are not canonically supported

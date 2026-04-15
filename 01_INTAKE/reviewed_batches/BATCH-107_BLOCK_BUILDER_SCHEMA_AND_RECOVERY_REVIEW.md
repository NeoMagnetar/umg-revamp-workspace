# BATCH-107 — Block Builder Schema and Recovery Review

## Batch Overview
- **Batch ID:** BATCH-107
- **Source type:** Derived extraction / handoff note
- **Review status:** REVIEWED
- **Disposition:** ACCEPT_AS_EVIDENCE
- **Primary domain:** block builder schema, validation, and recovery workflow
- **Canon status:** Not canonized
- **Reason for intake:** The source concentrates high-value implementation signal around schema design, block normalization, validation, folder organization, and Block Builder runtime assumptions.

## Source Snapshot
- The source describes recovery and stabilization work on the original UMG Block Builder after loss, reversion, and schema drift.
- The central work areas were schema design, large-scale patching, validation, folder organization, manifest instability, and builder-facing taxonomy.
- The source repeatedly treats the Block Builder as a system that must browse by library/category while still snapping and merging by MOLT role.
- The source is not a raw transcript. It is an extracted summary and must therefore be treated as evidence with preserved uncertainty.

## Chat-Level Summary
This batch captures a substantial data-layer and builder-foundation pass for UMG. It pushes toward a strict schema, normalized legacy blocks, validation-first workflows, safe reorganization practices, and CLI/bootstrap tooling for the Block Builder. It also exposes unresolved semantic and implementation tensions around whether `domain` belongs in schema, whether `Deployment` should exist as a main MOLT type, and how browsing taxonomy should coexist with MOLT-driven runtime behavior.

## UMG-Relevant Extraction

### Core semantic signal
- Blocks are modular units with both organizational identity and functional identity.
- Organizational identity is carried by domain/category/subcategory for browsing and library structure.
- Functional identity is carried by `molt_type` for snapping, merging, and runtime behavior.
- `prompt_template` and `body` are the two accepted content shapes in the working strict schema.
- `cantocore` is treated as compact identification and hinting logic, not the whole content model.
- `code_modules` are optional payload attachments and are not equivalent to semantic role.

### MOLT / block-builder signal
- Active working role set in this source:
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
- `Deployment` appears as a legacy role in the data layer but is explicitly treated as not acceptable as a main MOLT type.
- `Trigger` is semantically distinct from executable code payload.
- `CodeBlock` is defined here as a role for blocks whose primary payload is code or markup.

### Schema / composition signal
- Working strict required fields cluster around:
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
- `display.color` and `display.icon` are treated as builder UI essentials.
- Legacy-to-current normalization includes:
  - `content` → `body`
  - `code_modules[].path` → `code`
  - object-shaped `editable_fields` → array of strings
  - removal of legacy keys not allowed by strict schema

### Runtime / compiler-adjacent signal
- Concrete scripts named in the source:
  - `scripts/validate_blocks.py`
  - `scripts/autofill_block_fields.py`
  - `scripts/block_builder.py`
- Practical staged workflow:
  1. patch
  2. validate
  3. reorganize
  4. manifest
  5. builder UI
- Builder/runtime is expected to operate only on schema-clean blocks.
- Validation in CI is treated as the next necessary control layer to prevent future drift.

### Release / staging signal
- The source frames recovery as prerequisite work before restoring or rebuilding the lost Block Builder UI.
- It positions schema stabilization and safe reorganization as gating work before resuming Bolt or related interface rebuilding.

## Independent Review
This batch is high-value evidence for the control project because it ties abstract UMG semantics directly to a real builder data layer. It is especially important for Phase 1 and Phase 2 because it sharpens the distinction between browsing taxonomy and runtime MOLT role, while also surfacing direct compiler/documentation pressure around field legality, content shapes, and migration rules.

The source is also contradiction-heavy. It preserves instability around `domain`, `Deployment`, manifest behavior, script canon, and safe folder layout. Those contradictions should not be flattened. This batch is not a final schema decision. It is a strong evidence packet showing what the builder effort was converging toward, what failed, and what still needs explicit control-room adjudication.

## Roadmap Mapping
- **PHASE_1_CORE_ALIGNMENT**
  - MOLT role set pressure
  - Category vs MOLT runtime distinction
  - Trigger vs code payload distinction
  - `Deployment` as pseudo-role conflict
- **PHASE_2_COMPILER_IMPACT**
  - schema validator requirements
  - legacy patching / normalization
  - routing by metadata
  - strict-vs-flexible schema enforcement
- **PHASE_3_DOCUMENTATION_IMPACT**
  - schema v1.0 / v2.0 definitions
  - field glossary for prompt/body/code/display/snap/merge
  - builder-facing guidance on category browsing vs runtime semantics
- **PHASE_4_SKILL_ALIGNMENT**
  - CLI block builder as skill/bootstrap logic
  - CI validation workflow
  - preview-first safe reorg workflow
- **PHASE_5_PRD_AND_STAGING**
  - recovery sequencing before UI restoration
  - schema-clean library as prerequisite to Block Builder revival

## Action Outcome
- Accepted as evidence.
- Optional extracts added for:
  - compiler/runtime impact
  - blocks/MOLT/schema impact
  - contradiction flags
- No canon promotion performed.
- No schema decision finalized.
- Strong duplicate merge pressure exists with prior batches on metadata policy, schema drift, validation, and block routing.

## Recommended Next Decision
Adjudicate a single control-room decision on the builder data contract:
1. whether `domain` is canonical schema or folder-only organization,
2. whether `Deployment` is permanently disallowed as a main MOLT type,
3. whether strict schema migration is preferred over permissive runtime normalization.

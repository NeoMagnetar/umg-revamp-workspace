# BATCH-201 — PoeCore Phase 2 Setup — Review

## Batch Overview
- **Batch ID:** BATCH-201
- **Source Type:** derived repo-migration and architecture summary
- **Review Status:** REVIEWED
- **Disposition:** ACCEPT_AS_EVIDENCE
- **Primary Domain:** repo_structure_and_builder_runtime
- **Evidence Strength:** medium-high
- **Why it matters:** this batch captures a concrete migration toward one-file-per-block storage, clearer separation between blocks, stacks, manifests, schemas, and sleeves, and a more agent-usable repo structure for Poe integration.

## Source Snapshot
- The source centers on restructuring the `NEO-UMG-BUILDER` repo.
- Main work described:
  - splitting aggregated block dumps into individual `.block.json` files
  - treating `data/blocks/{MOLT_TYPE}/` as the single source of truth
  - regenerating manifests from canonical block files
  - separating stacks/sleeves/manifests/schema files
  - clarifying how Poe/NeoPoeUMG should function as a helper inside terminal and future web-builder flows
- The source also preserves unresolved tensions around `Deployment`, `Merge`, autoblocks, and builder/runtime semantics.

## Chat-Level Summary
This batch is a strong **repo-structure and builder-runtime migration artifact**. It is less about abstract UMG philosophy and more about operational maintainability: where block files live, how manifests are generated, how stacks differ from schemas, how sleeves differ from user-facing stack bundles, and how Poe should interact with the system as a helper agent. The key move is toward a canonical block tree under `data/blocks/`, with scripts and manifests aligned to that structure.

## UMG-Relevant Extraction
### Core Semantics
- `Snap / Stack / Merge` is treated as a central triad:
  - Snap = compatibility / adjacency
  - Stack = vertical grouped assembly
  - Merge = conflict resolution / precedence
- Template stack files are treated as MOLT-to-block-id maps rather than blocks.
- Distinction is sharpened between:
  - block files
  - stack/sleeve files
  - manifests
  - schema/config files

### Roles / Taxonomy
- Active MOLT folders listed:
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
- `Merge` remains questioned as a canonical MOLT type.
- `Deployment` remains present in folder structure, manifests, docs, and autoblocks, but its long-term canonical status is not fully settled.
- Definitions are increasingly operational:
  - Primary = root/core anchor
  - Subject = domain target
  - Instruction = execution logic
  - Philosophy = tone/ethos
  - Blueprint = layout/rendering
  - Directive = strategy/control
  - Trigger = event activation
  - Deployment = packaging/export/final-mile
  - Off = disabled/suppressed role

### Runtime / Compiler
- Canonical unit becomes one `.block.json` file under `data/blocks/{MOLT_TYPE}/`.
- Scripts aligned to canonical tree:
  - `consolidate_blocks.py`
  - `validate_blocks.py`
  - `generate_manifests.py`
  - `validate_manifest_refs.py`
  - `report_structure.py`
- Runtime path assumptions are being corrected toward:
  - `data/blocks`
  - `schema/`
  - `apps/umg-builder-web/manifests/`
- `poe_nl_agent.py` is treated as an NL-to-task runtime layer supporting file ops, block generation/merge, envoy generation/run.

### Sleeve / Stack / Builder Structure
- Distinction emerges between:
  - `/poe_core/sleeves/` for embedded/core sleeves
  - `/sleeves/` for user-facing stack bundles/templates
- Plan/chatbot/business stack files move toward semantically cleaner `.stack.json` placement.
- `webMatrix.json` becomes a schema/config concept rather than a builder output file.

### Agent / Skill Workflow
- Poe is positioned as a helper inside the repo/builder, not only as an external chat agent.
- Desired future role includes:
  - reading canonical block files
  - writing/validating block files
  - generating envoys
  - helping inside the builder UI
  - reasoning over manifests/stacks/schema files
- Envoys are treated as code-first, persistent sub-agents that may later become blocks.

## Independent Review
This batch is especially valuable because it pushes UMG toward a maintainable implementation surface:
- canonical per-block storage
- fewer duplicate sources of truth
- clearer boundaries between content blocks, templates, manifests, schemas, and sleeves
- stronger agent-usability inside a real builder/repo

Its main limits are semantic:
- `Deployment` status is still unsettled
- `Merge` status remains split between schema listing and runtime questioning
- `webMatrix.json` naming/placement was still confusing during cleanup
- Poe integration architecture inside the builder remains desired but not finalized

This should therefore be treated as evidence for migration direction and architecture cleanup, not as final canon on all type semantics.

## Roadmap Mapping
- **PHASE_1_CORE_ALIGNMENT:** clarify active MOLT roles and unresolved `Deployment`/`Merge` status
- **PHASE_2_COMPILER_IMPACT:** one-file-per-block storage, manifest generation, runtime path alignment, validator flow
- **PHASE_3_DOCUMENTATION_IMPACT:** schema reference reconciliation, manifest reference docs, sleeve/stack distinction docs
- **PHASE_4_SKILL_ALIGNMENT:** Poe helper integration, envoy generation, builder-facing agent workflows
- **PHASE_5_PRD_AND_STAGING:** builder ingestion path, canonical manifests, repo cleanup before deeper feature work

## Action Outcome
- Accepted as evidence.
- Default four-file pack created.
- Optional extracts created only for:
  - compiler/runtime pressure
  - blocks/MOLT taxonomy pressure
  - sleeve extraction
  - neostructure / layered repo-state pressure
  - contradiction / ambiguity tracking

## Recommended Next Decision
Decide whether `Deployment` remains a canonical MOLT type, becomes a meta/output layer, or moves into a separate schema/runtime category.

# BATCH-098_UMG_BLOCK_CREATION_PLAN_REVIEW

## Batch Overview
- **Batch ID:** BATCH-098
- **Short Topic:** UMG Block Creation Plan
- **Source Type:** Derived extraction / handoff note, not raw transcript
- **Review Status:** REVIEWED
- **Disposition:** ACCEPT_AS_EVIDENCE
- **Primary Domain:** metadata-governed domain block ingestion and library organization
- **Confidence Note:** This batch is concrete and operationally useful, but provenance remains limited because it is a summarized extraction of an earlier conversation rather than the raw exchange itself.

## Source Snapshot
- Source title: `098 UMG Block Creation Plan`
- Source character: summarized extraction of a prior conversation
- Main themes surfaced by source:
  - conversion of a business-planning source corpus into modular UMG blocks
  - adoption of a formal UMG Block Metadata Policy (v1.0)
  - additive one-section-at-a-time block-library growth
  - explicit MOLT assignment by block function
  - category-path organization and cumulative export readiness
- Provenance caution:
  - the source reports adopted policy and produced examples, but the actual underlying files and raw generation steps are not included here.

## Chat-Level Summary
This batch presents a practical content-ingestion workflow for UMG rather than a purely conceptual architecture discussion. The source describes how a domain document, the “Master Builder Citadel” business-planning corpus, was converted into reusable UMG blocks governed by a locked metadata policy. It defines a standard metadata envelope for every block, maps MOLT roles to domain block classes, introduces category-path organization for a cumulative block library, and treats triggers, ledger fields, overlay fields, and export configuration as first-class parts of reusable block composition. The batch is especially valuable because it grounds UMG in a concrete builder/app use case and pressures the project to standardize metadata, block IDs, export retention rules, and additive ingestion behavior.

## UMG-Relevant Extraction
### Core semantics
- UMG is used here as a reusable modular block system for a business / web app / chatbot builder.
- Blocks are intended to be organized, injection-ready, and reusable across the app.
- The workflow is additive: block sets accumulate over time rather than being regenerated from scratch.
- Domain content is being translated into UMG blocks rather than remaining only as prose documentation.

### MOLT / block signal
- The metadata policy includes a strict `molt_type` field:
  - Primary
  - Instruction
  - Philosophy
  - Subject
- In the source conversation:
  - plan types were assigned to Primary
  - subtypes / formats were assigned to Instruction
  - future embedded report / section blocks were proposed for Subject
- This creates concrete domain-to-MOLT mapping pressure rather than only abstract taxonomy talk.

### Metadata governance signal
- Every block is expected to carry a fixed metadata envelope including:
  - block_id
  - label
  - category
  - description
  - editable_fields
  - molt_type
  - tags
  - canto_overlay
  - ledger
  - trigger
  - export_config
- Metadata is treated as governance, provenance, interoperability, and traceability infrastructure.
- Display behavior is intentionally separated from retained attribution metadata.

### Runtime / compiler signal
- Trigger behavior is explicit and attached to use/fork events.
- Blocks are described as injection-ready and fork-ready, implying runtime assembly and mutation surfaces.
- The ingestion model is additive and section-based, which pressures library update semantics.
- Category paths imply structured retrieval and organization of blocks at runtime or build time.

### Stack / architecture signal
- The source asks for skeleton-tree / branched organization.
- Category paths imply hierarchical library structure by domain and function.
- The library behaves more like a growing block inventory than isolated single exports.

### Workflow / skill signal
- User provides policy and format.
- Assistant converts one source section at a time into blocks.
- JSON copies and category structure are preserved as part of the workflow.
- End-of-message organizational overlay is required as a recurring process layer.

## Independent Review
This batch is high-value because it moves UMG from abstract architecture into disciplined block production. The strongest extract is not one single semantic phrase, but the combination of three operational commitments: a locked metadata policy, additive section-by-section ingestion, and category-path organization for exportable block libraries.

The **UMG Block Metadata Policy (v1.0)** is the most durable contribution in the batch. It pressures the project to define what every block must retain regardless of UI, export destination, or remix context. That directly affects documentation, compiler/runtime loading assumptions, and future content-tooling.

A second important signal is the **functional mapping of domain blocks into MOLT roles**. Even though not all assignments are independently user-audited in the source summary, the batch shows a live example of how Primary, Instruction, and potentially Subject can be assigned by content role rather than by generic theory.

The biggest caution is that some implementation details in example blocks may reflect assistant-shaped defaults rather than stabilized canon. That means Stage 1 should preserve the workflow and schema pressure without prematurely canonizing every example field value.

## Roadmap Mapping
### PHASE_1_CORE_ALIGNMENT
- pressures definition of:
  - block metadata canon
  - MOLT role assignment by functional block class
  - overlay vs metadata separation
  - block ID and lineage expectations

### PHASE_2_COMPILER_IMPACT
- pressures need for:
  - additive section-by-section ingestion
  - library/category-path loading behavior
  - trigger and fork-event support
  - export-retention guarantees
  - interlinking through ledger, trigger, and overlay fields

### PHASE_3_DOCUMENTATION_IMPACT
- pressures need for:
  - formal metadata policy documentation
  - domain block creation guide
  - UI-display versus retained-metadata explanation
  - category-path naming conventions

### PHASE_4_SKILL_ALIGNMENT
- suggests:
  - section-to-block conversion workflows
  - organizational overlay discipline
  - block-generation skills that preserve metadata policy by default

### PHASE_5_PRD_AND_STAGING
- suggests:
  - business-plan builder modeled as block inventory
  - staged category expansion rather than full one-shot generation
  - exportable, metadata-rich content modules for app injection

## Action Outcome
- **Disposition chosen:** ACCEPT_AS_EVIDENCE
- **Why:** the batch is concrete, operational, and strongly relevant to future UMG tooling, but it remains a derived summary and not direct proof of finalized canon or persisted implementation.
- **Optional extracts justified:**
  - `COMPILER_EXTRACT` because the source contains additive ingestion, trigger, export, and library-loading implications.
  - `BLOCKS_MOLT_EXTRACT` because the batch strongly pressures standardized block metadata, MOLT role mapping, and block schema discipline.

## Recommended Next Decision
Decide whether the UMG Block Metadata Policy (v1.0) should be promoted into documentation-first synthesis as the default block-governance baseline, or held as provisional evidence until block ID, overlay semantics, and export behavior are reconciled across other ingestion workflows.

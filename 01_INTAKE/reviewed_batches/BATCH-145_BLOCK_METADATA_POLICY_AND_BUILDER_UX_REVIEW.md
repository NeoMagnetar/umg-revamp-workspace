# BATCH-145 — Block Metadata Policy and Builder UX Review

## Batch Overview
Batch ID: BATCH-145  
Source Type: derived summary / block metadata policy, builder UX, and hackathon-scope consolidation  
Working Topic: block metadata policy, visible MOLT semantics, trigger schema, snap/merge builder behavior, CantoCore overlay, non-Web3 hackathon staging  
Review Status: REVIEWED  
Disposition: ACCEPT_AS_EVIDENCE

## Source Snapshot
The source is a structured consolidation of a chat focused on designing a UMG-powered block-builder application for business planning, website/app generation, and chatbot/agent composition.
The work centered on turning large category lists into modular block inventories and then clarifying how those blocks should be:
- understood
- viewed
- stored
- inspected
- triggered
- exported
- used inside a builder interface

A major contribution was the introduction of a formal `UMG Block Metadata Policy (v1.0)` with structured fields, trigger schema, attribution policy, display behavior, and export behavior.
The conversation also pushed for more visible MOLT semantics, proposed a “View MOLT” / MOLT Lexicon HUD, explored CantoCore overlays and recursive/self-describing block behavior, and repeatedly constrained the hackathon version away from full Web3 implementation.
Because the source is a derived summary rather than a separately ratified canon spec, it should be treated as strong evidence of block-policy direction, builder UX principles, and implementation-ready metadata design, but not as automatic canon.

## Chat-Level Summary
This batch is strongest as a practical block-policy and builder-interface source.
Its central contribution is treating the block as the foundational modular unit of the system and then making that block inspectable, editable, triggerable, exportable, and intelligible to both casual users and developers.

The strongest reusable signal is the metadata-policy layer.
Rather than leaving blocks as loose labels, the chat gives them a structured schema surface:
label,
category,
description,
editable fields,
MOLT type,
tags,
overlay,
ledger,
trigger,
and export behavior.
That materially advances UMG from conceptual modularity toward a coherent builder artifact model.

The second major contribution is visibility.
The user explicitly wanted MOLT to be surfaced more clearly.
In response, the chat proposed UX ideas such as a MOLT Lexicon HUD / “View MOLT” mechanism so a person could inspect a block’s normal meaning and its UMG/MOLT meaning together.
That makes the batch especially useful for builder transparency and documentation.

A third strong contribution is staging discipline.
The chat repeatedly constrains the current version to a practical Bolt hackathon build without full Web3 dependency, while preserving future expansion room.
That is important project-boundary evidence.

## UMG-Relevant Extraction
Blocks are treated as foundational modular units for cognition, planning, and generation.
A block is framed as a reusable logic/documentation unit with fields such as:
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

The system goal is not just content storage.
It is compositional logic:
blocks snap,
merge,
stack,
trigger,
and export into usable plans, code structures, or configurations.

`molt_type` is explicitly used in metadata.
The policy defines `molt_type` values as:
- `Primary`
- `Instruction`
- `Philosophy`
- `Subject`

The assistant also mapped block fields into MOLT-aware interpretation, such as:
- `name` / `label` as identity-level reference
- `editable_fields` as instruction-layer surface
- `default_template` as render/generative structure

The user observed that MOLT reference was not visible enough in the current block system.
The proposed response was a “MOLT Lexicon HUD” / “View MOLT” block inspector that would surface structural meaning without overwhelming the normal interface.

Trigger logic was formalized through a `trigger` object with:
- `type`
- `action`
- `conditions`
- `next_block`

Trigger types listed:
- `on_click`
- `on_submit`
- `on_load`
- `on_custom_event`

Triggers are described as optional but recommended for instruction-type or flow-dependent blocks.
The broader builder logic also assumes triggering through snaps, user input, file uploads, or plan-type selections.

Merge logic was repeatedly emphasized.
The builder was designed so blocks can snap together and merge.
A `merge_candidates` concept appeared, along with SnapEngine++ / block fusion logic where:
- matching blocks can highlight merge opportunities
- merged blocks can inherit fields and combined templates
- merged blocks can retain merge history

The source strongly separates:
- block metadata / internal structure
- builder UI display
- export rendering
- MOLT inspection view

Metadata is treated as something retained in exports even if not always shown in the standard user interface.
This is strong blueprint/rendering separation evidence.

The chat also introduced a runtime/status overlay concept:
CantoCore status could examine current task, broad project, completed stages, next required steps, files in scope, and system path.
This functions like runtime workflow tracking and project-state introspection rather than static block content.

The hackathon build direction is explicit:
focus on business/web/chatbot builder logic,
make the system public-facing and understandable,
defer Web3/blockchain implementation for now,
and preserve future marketplace or crypto direction without forcing it into the current release.

## Independent Review
This batch has high Stage 1 value because it gives the project a concrete policy and UX direction for blocks rather than only high-level modular rhetoric.
The strongest contribution is the metadata-policy structure.
That is the most implementation-ready artifact in the batch.

The visibility push is also especially important.
Without stronger MOLT visibility, blocks risk becoming generic configurable tiles rather than UMG-meaningful units.
The proposed MOLT inspector / HUD therefore matters as much as the raw metadata fields.

The bounded hackathon scope is the third strong contribution.
It keeps the current product legible and practical while preserving future expansion options.
That is good staging discipline.

Main cautions:
- MOLT visibility remains a problem statement plus interface proposal, not yet a solved implementation
- some generated files in the underlying chat used simplified schemas in places while the policy described a richer schema
- CantoCore / CyentoCore relation to current block format remained partially unresolved
- NeoBlock / NeoStack / sleeve language stayed adjacent rather than directly formalized in this chat
- many runtime/compiler behaviors remain proposal-level

## Roadmap Mapping
Primary domain: block metadata policy, MOLT visibility, and builder transparency/staging

Roadmap phases touched:
PHASE_1_CORE_ALIGNMENT
PHASE_2_COMPILER_IMPACT
PHASE_3_DOCUMENTATION_IMPACT
PHASE_4_SKILL_ALIGNMENT
PHASE_5_PRD_AND_STAGING
PHASE_7_RELEASE_READINESS

Key phase implications:
Phase 1: supports clearer block ontology and visible MOLT semantics.
Phase 2: provides a concrete metadata schema, trigger object, and snap/merge runtime direction.
Phase 3: offers documentation-ready policy language and user/developer explanation patterns.
Phase 4: informs skill and builder workflows through CantoCore task-status overlays and metadata-driven behavior.
Phase 5: contributes PRD-grade hackathon staging rules and builder UX requirements.
Phase 7: supports release clarity by explicitly scoping the current version away from premature Web3 dependency.

## Action Outcome
Accepted as evidence.
Frozen as a Stage 1 intake pack.
Optional compiler extract, blocks/MOLT extract, canon candidates, and contradiction flags are justified because the source contains a practical metadata policy, trigger schema, visibility doctrine, and unresolved builder/runtime tensions.

## Recommended Next Decision
Control-room review should decide how to normalize and promote:
1. the UMG Block Metadata Policy field set
2. visible MOLT inspection rules
3. trigger-object standardization
4. metadata-retention versus UI-display behavior
5. hackathon-scope non-Web3 staging language

# BATCH-029 — Persona Layer and Trigger Extension Ingest Review

## Batch Overview
- **Batch ID:** BATCH-029
- **Short Topic:** Persona layer and Trigger-library extension ingest
- **Source Type:** Derivative summary / handoff-style extraction, not raw transcript
- **Review Status:** REVIEWED
- **Disposition:** ACCEPT_AS_EVIDENCE
- **Canon Status:** Not canon; evidence only
- **Optional Extracts Added:** Compiler extract, Blocks/MOLT extract

## Source Snapshot
- The source describes a chat with two connected threads:
  1. review of a Persona / Communication Style Library artifact
  2. drafting OpenClaw ingestion instructions for a Business Trigger Blocks extension
- The persona portion audits architectural fit inside UMG.
- The trigger portion defines a recurring ingest rule for future Trigger-type block drops.
- Because the visible source is a summary rather than the full thread, this review preserves any unresolved ambiguity instead of inferring missing detail.

## Chat-Level Summary
- The batch argues that persona or communication style should not sit inside the core reasoning substrate.
- MOLT / NeoBlocks / NeoStacks are framed as the layers that govern cognition, method, priority, and structure.
- Persona is instead framed as a surface-expression layer that applies after cognition and blueprint choice but before final text emission.
- The second thread turns to maintenance of the Trigger library, specifically a business-domain extension covering `TRG.101` through `TRG.200`.
- The ingest rule is deterministic: preserve exact IDs, keep Trigger-type blocks inside the Trigger category, preserve section grouping, avoid renumbering, compression, or cross-category drift.

## UMG-Relevant Extraction
### Persona Layer
- Persona is treated as **modulation**, not core reasoning.
- Personas should not override clarity, task fit, or trust in high-stakes domains.
- To become runtime/compile-ready, persona entries need operational metadata and explicit conflict/suppression logic.
- The recommended runtime order is:
  1. solve cognition with MOLT + NeoBlocks + NeoStacks
  2. determine blueprint / output format
  3. apply persona modulation profile
  4. emit final surface text

### Trigger Extension Ingest
- Trigger extensions are treated as category-specific block-library growth, not as freeform content.
- `TRG.101–TRG.200` is framed as a business Trigger extension range.
- Ingestion must preserve:
  - exact IDs
  - category fidelity
  - grouping by business-domain section
  - non-duplication with legacy ranges
- This implies a recurring OpenClaw maintenance workflow for future typed block drops.

### Structural Significance
- The batch contributes to two different UMG surfaces:
  - runtime layering: cognition vs style/output modulation
  - library maintenance: deterministic ingest discipline for block extensions
- Both themes support maintainability, auditability, and bounded behavior.

## Independent Review
- This is a strong evidence batch for separating **what the system reasons** from **how the answer is voiced**.
- It also contributes a clean operational rule for ingesting Trigger-library expansions without damaging identifier stability.
- The persona side is architecturally important but explicitly not ready for direct compiler/runtime adoption without more metadata and precedence rules.
- The trigger-ingest side is more operationally mature and could be turned into documented workflow guidance with relatively little transformation.
- No part of the batch should be promoted automatically into canon because:
  - the persona precedence model is still incomplete
  - blend/conflict/suppression behavior is not fully formalized
  - the trigger rule is strong but still derived from a summarized source artifact rather than a finalized control-room decision

## Roadmap Mapping
### Primary Phases Touched
- **PHASE_1_CORE_ALIGNMENT**
  - separation of cognition from style modulation
  - clarification that persona is not a MOLT role or NeoStack
- **PHASE_2_COMPILER_IMPACT**
  - persona metadata requirements
  - suppression / fallback / conflict logic
  - deterministic typed block ingest rules
- **PHASE_3_DOCUMENTATION_IMPACT**
  - runtime order documentation
  - ingest rule documentation for future block-library extensions
- **PHASE_4_SKILL_ALIGNMENT**
  - OpenClaw should detect typed block uploads and route Trigger files appropriately
- **PHASE_5_PRD_AND_STAGING**
  - persona library maturity staged below production-ready runtime use

### Duplicate / Conflict Pressure
- **Duplicate pressure:** high with earlier batches around sleeve governance, routing determinism, compiler-ready identifiers, and modular architecture
- **Contradiction watch:** medium because persona precedence relative to sleeve defaults remains unresolved

## Action Outcome
- Accepted as evidence.
- Frozen into a Stage 1 pack.
- Optional extracts added only where the source clearly supports them:
  - compiler extract
  - blocks/MOLT extract

## Recommended Next Decision
- Decide whether UMG canon will formally define **persona as a post-cognition surface modulation layer** with explicit precedence relative to sleeve defaults.
- Decide whether typed block-ingest rules should become a standard compiler/documentation rule for future MOLT library extensions.

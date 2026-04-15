# BATCH-073 — Commando UMG Bot Plan Review

## Batch Overview
- **Batch ID:** BATCH-073
- **Short Topic:** Commando bot plan / Inventory Console / Loadout Library
- **Source Type:** Derived handoff summary, not a raw chat transcript
- **Review Status:** REVIEWED
- **Disposition:** ACCEPT_AS_EVIDENCE
- **Primary Domain:** UI composition and runtime-facing loadout architecture

## Source Snapshot
- One uploaded summary titled **"073 Commando UMG Bot Plan"**
- Source focus:
  - React-based Inventory Console UI
  - block CRUD and loadout persistence
  - Loadout Library / archive concepts
  - export pipeline toward deployable agent artifacts
- Evidence quality note:
  - strong implementation-direction signal
  - moderate formal-spec confidence
  - unresolved runtime / compiler law

## Chat-Level Summary
This batch translates UMG into a concrete UI-layer composition system. It presents blocks as user-editable modular units, groups them into loadouts, and treats those loadouts as reusable composed configurations that can later be saved, exported, and deployed. The strongest value of the batch is not finalized doctrine, but a practical surface for composition, persistence, and packaging.

## UMG-Relevant Extraction

### Core Semantics
- Blocks were treated as discrete modular units with a type and description.
- Loadouts were treated as grouped block sets representing composed configurations.
- The system remained faithful to modular construction rather than monolithic prompting.
- The UI implied later execution or export rather than direct runtime resolution inside the interface.

### MOLT / Block Roles
- Explicit role set present in the UI:
  - Primary
  - Subject
  - Merge
  - Instructions
- The role set aligns partially with known UMG role language, but is not complete.
- Blueprint was not explicitly represented as a selectable block type.

### Bundle / NeoStack Surface
- Loadout functions as a reusable bundle unit.
- Loadout also behaves like a proto-NeoStack:
  - ordered block array
  - editable composition surface
  - persistence and retrieval
- The exact canonical relationship between **bundle**, **loadout**, and **NeoStack** was not finalized here.

### Compiler / Runtime Surface
- Implied flow:
  - UI composition
  - save loadout
  - export package
  - external runtime consumption
- The source strongly suggests a compiler-adjacent surface but does not implement merge law, priority, preview, or execution semantics.
- Replit Template Uploader implies an external execution context consuming saved artifacts.

### Governance / Constraints
- Hard UI limit: `MAX_BLOCKS = 8`
- Save requires both loadout name and at least one block.
- No deeper governance model was defined beyond UI validation.

### Documentation / Product Surface
- The UI naming layer contributes implementation-facing terminology:
  - Inventory Console
  - Loadout Builder
  - Loadout Library
  - Block Archive
- These names are useful evidence for PRD and staging, but not final canon.

## Independent Review
This is a strong Stage 1 batch for implementation-facing evidence. It gives a concrete composition interface, persistence model, and export workflow that help bridge abstract UMG structure into a usable builder surface. The batch is especially relevant to compiler-adjacent thinking because it shows where users compose structures before execution.

The source is still derivative and partially prototype-oriented. It does **not** settle role completeness, execution order, priority, merge behavior, or Blueprint handling. It should therefore be retained as evidence for synthesis, not promoted to canon.

## Roadmap Mapping
- **PHASE_1_CORE_ALIGNMENT**
  - role completeness questions
  - loadout vs bundle vs NeoStack terminology
- **PHASE_2_COMPILER_IMPACT**
  - composition surface
  - export boundary
  - missing merge / priority / preview logic
- **PHASE_3_DOCUMENTATION_IMPACT**
  - naming normalization
  - UI terminology
  - block role descriptions
- **PHASE_4_SKILL_ALIGNMENT**
  - packaging flow for agent-oriented configurations
- **PHASE_5_PRD_AND_STAGING**
  - Inventory Console as prototype composition interface
  - deployment/export implications

## Action Outcome
- Retained as **ACCEPT_AS_EVIDENCE**
- Default four-file Stage 1 pack created
- Optional extracts created:
  - `BATCH-073_COMPILER_EXTRACT.md`
  - `BATCH-073_BLOCKS_MOLT_EXTRACT.md`

## Recommended Next Decision
Decide whether **Loadout** should become:
1. a UI-only storage term,
2. a formal alias for a reusable bundle, or
3. a frontend representation of a NeoStack with explicit runtime mapping.

A linked follow-up decision is whether the UI role set must add explicit **Blueprint** and **Priority** support before this surface is treated as a canonical UMG composition interface.

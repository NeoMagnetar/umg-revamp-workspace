# BATCH-007 — Reviewed Batch
## Batch Overview
- **Batch ID:** BATCH-007
- **Short Topic:** instruction topology, neutral base sleeve, missing anchor artifacts
- **Source Type:** extracted chat summary with project-file grounding
- **Disposition:** evidence only, not canon
- **Primary Domain:** instruction topology / governance layering
- **Optional Extracts Included:** compiler, sleeve, blocks/MOLT

## Source Snapshot
- The batch focuses on cleaning up UMG instruction topology before reducing it into CyentCore.
- It separates governance, project instructions, memory, user preferences, sleeves, MOLT maps, tags, and project files into distinct authority layers.
- The dominant architectural move is replacing a design-trapped base state with a neutral UMG base sleeve that can host explicit modes without auto-entering them.
- The batch also explains messy system checks as an artifact-gap problem: missing anchor files such as a base sleeve, tag semantics, NL sleeve block, and MOLT map schema.

## Chat-Level Summary
This batch is a topology-and-artifacts cleanup pass rather than a new semantic invention pass. Its central claim is that UMG already has most of the right ideas, but the instruction layers and anchor files are not cleanly separated. The result is ambiguity around what is authoritative, what is remembered, what is current-turn context, and what is merely reference material. The batch therefore proposes a neutral governed base sleeve, a strict division of responsibilities across instruction layers, and a minimum NL-first project file set so later CyentCore reduction can happen on stable ground.

## UMG-Relevant Extraction
### 1. Core semantic signal
- UMG should be substrate/framework first, with personas added later rather than embedded as the base identity.
- Sleeves define what exists; MOLT maps define what is happening now; tags are recall-only; files are reference-only unless explicitly promoted.
- Memory should store durable process law, not runtime state.
- NL-first clarification is treated as the correct step before syntax compression or CyentCore reduction.

### 2. Base-sleeve and resleeving signal
- The current design-only base state is treated as the wrong default because it traps the system in one permanent posture.
- A new neutral base sleeve is proposed: `UMG_BASE` / `umg_base.core`.
- This base sleeve should be active, governed, and idle by default.
- Design, inspection, execution, mutation, and resleeving should become explicit subordinate modes or overlays rather than the permanent base identity.

### 3. Governance and authority-layer signal
- Governance is mapped to hard law/invariants only.
- User preferences are mapped to blueprint/output style only and must not alter scope or permissions.
- Project files are reference/tooling surfaces, not automatically authoritative instructions.
- Authority flows downward: lower layers should not silently override higher-authority layers.

### 4. Artifact-gap and system-check signal
- The batch diagnoses messy checks as missing-anchor artifacts rather than missing theory.
- Proposed minimum file anchors:
  - `canon/umg_process_law.nl.md`
  - `sleeves/umg_base_sleeve.nl.md`
  - `context/molt_map.nl.md`
  - `tags/tag_semantics.nl.md`
  - `system_checks/system_check_protocol.nl.md`
- System checks should reference these anchors explicitly instead of improvising around their absence.

## Independent Review
This batch is high-value because it does not try to solve UMG by adding more layers. It solves a narrower but foundational problem: unclear placement of authority, memory, reference files, current-turn context, and base identity. That makes it especially important for project hygiene, safer mode handling, and future documentation/compiler consistency.

The strongest project value is the combined effect of:
- a neutral governed base sleeve instead of a permanent design sleeve
- durable process-law language suitable for memory
- a strict sleeve-versus-MOLT distinction
- clear non-authoritative status for tags and files unless promoted
- a concrete minimum anchor-file set for cleaner checks and later reduction

The main caution is that this batch is still largely NL-first and topology-oriented. It proposes structure and artifacts, but it does not yet fully validate those artifacts against repo contents or compiler integration. It is therefore strong Stage 1 evidence, but not yet a final implementation contract.

## Roadmap Mapping
- **Phase 1 — Core Alignment:** strongly supports sleeve vs mode, governance vs style, memory vs runtime state, and files vs canon separation.
- **Phase 2 — Compiler Impact:** supports explicit handling of MOLT map schemas, tag semantics, and missing-anchor validation in system checks/runtime protocols.
- **Phase 3 — Documentation Impact:** strongly supports base-sleeve documentation, process-law artifacts, tag semantics docs, and NL-first anchor files.
- **Phase 4 — Skill Alignment:** supports explicit activation-only workflows and safer base-state behavior for sleeve-hosting skills.
- **Phase 5 — PRD and Staging:** contributes staging logic: stabilize NL artifacts first, improve checks second, reduce/compress later.

## Action Outcome
- Accepted as evidence.
- Frozen into a Stage 1 intake pack.
- Routed toward sleeve, blocks/MOLT, and compiler/runtime-adjacent follow-up surfaces.
- Not promoted to canon.

## Recommended Next Decision
Lock the contract for:
1. **neutral UMG base sleeve semantics**
2. **process-law memory boundaries**
3. **MOLT map schema role and persistence rules**
4. **minimum anchor-file set required for clean system checks**

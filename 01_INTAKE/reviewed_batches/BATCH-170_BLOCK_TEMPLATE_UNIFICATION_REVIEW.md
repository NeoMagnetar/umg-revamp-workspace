# BATCH-170 Block Template Unification Review

## Batch Overview
- **Batch ID:** BATCH-170
- **Source Title:** UMG block template review
- **Stage:** Stage 1 intake
- **Disposition:** ACCEPT_AS_EVIDENCE
- **Evidence Status:** Non-canonical intake artifact
- **Primary Value:** Taxonomy and schema-unification audit for UMG block templates

## Source Snapshot
This source reviews a block-template conversation centered on a Google Doc called **UNIVERSAL BLOCK LIST**. The discussion moved from explaining block template roles into a wider unification pass covering block semantics, common schema anatomy, merge hierarchy, naming overlap, snap behavior, policy layers, orchestration blocks, and compiler/runtime normalization needs.

## Chat-Level Summary
The source treats UMG blocks as modular units with a shared anatomy and distinct semantic roles. It identifies both stable-looking roles and unstable overlaps, especially around:
- Directive vs Instruction
- Philosophy vs Blueprint
- Merge as block type vs merge as engine behavior
- policy layers versus ordinary content layers
- active canonical blocks versus dormant or experimental blocks

The source is strongest as a **schema and terminology normalization audit**, not as final canon. It is useful because it preserves tensions explicitly instead of pretending the block inventory is already harmonized.

## UMG-Relevant Extraction
### Stable or strong signals
- Shared block anatomy was explicitly proposed: `id`, `name`, `molt_type`, `purpose`, `content`, `inputs`, `outputs`, `overlays`, `merge`, `snap`, `metadata.ledger`.
- Primary, Subject, Instruction, Philosophy/Blueprint, and policy layers were treated as recurring anchor concepts.
- Alignment and Privacy were treated as special override-capable policy layers outside normal content merge.
- Stack order, horizontal overlays, and snap/merge behavior were treated as compiler/runtime concerns rather than just UI choices.

### Key tensions preserved
- **Directive vs Instruction** remains unresolved.
- **Philosophy vs Blueprint** remains unresolved.
- **Merge block vs merge engine logic** remains unresolved.
- **Priority order** is not fully stable because earlier and later explanations differ.
- Several listed block families appear to be adjacent, dormant, or experimental rather than clearly canonical.

## Independent Review
This source should be retained because it gives the project a concentrated record of where block language is stable and where it drifts. It is particularly useful for:
- semantic alignment work
- schema guide revision
- compiler/runtime normalization
- later PRD backlog formation

It should **not** be treated as direct canon because the chat mixes extraction with design recommendation. Several schema proposals are assistant-generated and should remain evidence until explicitly reconciled.

## Roadmap Mapping
- **Phase 1 — Core Alignment:** very strong impact; clarifies which block roles are stable and which need naming decisions.
- **Phase 2 — Compiler Impact:** strong impact; merge/snap metadata, priority order, and policy-layer override behavior need formal runtime handling.
- **Phase 3 — Documentation Impact:** very strong impact; calls for terminology cleanup, family grouping, and unified schema documentation.
- **Phase 4 — Skill Alignment:** moderate impact; clearer block taxonomy would help agent/runtime modules such as Routing, Deployment, RAG, and Failsafe.

## Cross-File Synthesis
This batch reinforces a recurring UMG pattern: the project often has strong conceptual structure but inconsistent public naming. Here that appears in block template language. The source does not settle the ontology, but it cleanly marks the exact seams where normalization work is needed.

## Action Outcome
- Accepted as evidence
- Promoted into Stage 1 artifact pack
- Optional extracts created for:
  - Blocks/MOLT
  - NeoStructure
  - Compiler
  - Canon Candidates

## Recommended Next Decision
Decide whether the project wants one public canonical vocabulary for:
1. Directive vs Instruction
2. Philosophy vs Blueprint
3. Merge block vs merge engine
4. Policy layers as ordinary blocks versus higher-order controls

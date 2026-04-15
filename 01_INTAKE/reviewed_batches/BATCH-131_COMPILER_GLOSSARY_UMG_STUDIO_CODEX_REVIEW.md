# BATCH-131 — Compiler Glossary · UMG Studio Codex Review

## Batch Overview
Batch ID: BATCH-131  
Source Type: derived summary / Studio v1 product-spec consolidation, not a raw transcript  
Working Topic: Studio panel architecture, constrained editing model, one-active-sleeve workflow, bundle/merge/compress behavior, governance scope, compiled sleeve file format, repo/package structure  
Review Status: REVIEWED  
Disposition: ACCEPT_AS_EVIDENCE

## Source Snapshot
The source is a structured consolidation titled `Branch (Compiler Glossary) · UMG Studio Codex`.
It summarizes a chat focused on translating UMG semantics into a concrete Studio v1 authoring environment.
The source refines how UMG entities should be visualized, edited, saved, compiled, and exported inside Studio, while preserving a strong boundary between UI behavior and compiler truth.
Because the source is a derived summary rather than a raw transcript or direct code diff, it should be treated as strong evidence of intended Studio/product direction, but not as automatic canon.

## Chat-Level Summary
This batch is the strongest Studio-facing Stage 1 source in the current run.
Its central move is to constrain Studio so the UI reflects UMG grammar instead of encouraging freeform graph manipulation.
The graph becomes a map rather than an editing engine, while actual mutation is pushed into explicit panel-based flows.
The batch sharply limits structural operations:
bundle and merge are same-MOLT in v1,
compress is a distinct column-to-NeoBlock packaging step,
governance operates only at NeoStack scope,
and mobile is intentionally view-only for structure.
It also defines a practical product shell:
one active Sleeve at a time,
clear left/center/bottom/right panel responsibilities,
explicit compile states,
and a compiled sleeve file format that preserves layout metadata without turning layout into compiler semantics.

## UMG-Relevant Extraction
The active Sleeve is the primary working document and the unit loaded, edited, compiled, saved, and exported.
Studio is built around one active Sleeve at a time.
The graph or matrix is a spatial reflection of structure, not the source of semantic truth.
Editing is explicit and panel-based; the graph is for overview, arrangement, and selection.
MOLT hierarchy remains authoritative within a column.
A MOLT column is a vertical ordered set of blocks intended to become a NeoBlock.
Blocks remain tied to their MOLT type lane and cannot change type through movement.
Cross-MOLT changes are explicit edit operations, not movement operations.
Bundle is constrained to same-MOLT selections in v1.
Merge is also simplified to same-MOLT in v1.
Priority is decomposed into:
MOLT hierarchy,
rank/order within a MOLT lane,
priority tags across sibling NeoBlocks in a NeoStack,
and governance override above normal priority.
Default priority is Medium for blocks and NeoBlocks.
Bundle and merge replace originals with a new composite result while preserving internal provenance.
Compress is separate from merge and bundle; it packages exactly one column into one NeoBlock.
NeoBlocks become the main movable units in the graph.
NeoStacks are grouping structures for multiple NeoBlocks within a Sleeve and serve as governance scope for peer conflicts.
Governance is simplified in v1 to scoped priority override within a NeoStack.
Governance cannot change MOLT type, reorder blocks in a column, act directly on raw blocks, or create/merge/bundle/compress entities.
Strong panel separation is established:
left = navigation/assets,
center = graph/overview,
bottom = editing/operations,
right = compiler I/O, diagnostics, and controlled JSON apply/revert.
Compile is explicit, not automatic.
Compile states are defined.
Runtime, Trace, Raw, Input JSON, Governance, Block Inspector, and Stats/Hash surfaces are specified.
A compiled sleeve file format is defined that includes sleeve data, layout, compile outputs, and hashes, while keeping layout metadata out of compiler semantics.
Mobile is intentionally restricted to view-only graph plus content editing, with no structural mutation.

## Independent Review
This batch has high Stage 1 value because it operationalizes UMG semantics into product behavior without collapsing UI actions into compiler truth.
The strongest contribution is the disciplined separation of:
semantic editing,
structural packaging,
graph visualization,
compiler execution,
and storage/export behavior.
The simplification of v1 toward same-MOLT bundle/merge and NeoStack-scoped governance is strategically useful because it reduces the risk of Studio becoming a semantic improvisation surface before core compiler semantics are fully stable.
The “graph is the map, not the engine” framing is especially valuable because it can likely prevent a large amount of future UX-driven semantic drift.
The batch also carries strong release value through its portable compiled sleeve file format, panel contracts, and one-active-sleeve workflow.
Main caution: some visual and architectural details remain product-direction evidence rather than final canon, especially around graph/matrix form, NeoStack display style, tag-trigger dominance, and repo shape.

## Roadmap Mapping
Primary domain: Studio v1 authoring architecture with direct compiler-boundary implications

Roadmap phases touched:
PHASE_1_CORE_ALIGNMENT
PHASE_2_COMPILER_IMPACT
PHASE_3_DOCUMENTATION_IMPACT
PHASE_4_SKILL_ALIGNMENT
PHASE_5_PRD_AND_STAGING
PHASE_6_GITHUB_EXECUTION
PHASE_7_RELEASE_READINESS

Key phase implications:
Phase 1: reinforces semantic boundaries between hierarchy, priority, governance, and composition operations.
Phase 2: constrains how Studio must emit compiler-safe structures and compiled sleeve artifacts.
Phase 3: provides contract-ready documentation language for panel roles, editing constraints, and file format behavior.
Phase 4: affects any skill or assistant workflow that helps author, compile, or edit Studio content.
Phase 5: provides direct PRD/product structure for v1 Studio.
Phase 6: informs repo/package isolation between Studio and compiler.
Phase 7: supports a publishable product direction by simplifying behavior and narrowing mutation surfaces.

## Action Outcome
Accepted as evidence.
Frozen as a Stage 1 intake pack.
Optional compiler extract, canon candidates, and contradiction flags are justified because the batch contains concrete product contracts, compiler-boundary behavior, and several explicit simplifications and deferred features that need preservation.

## Recommended Next Decision
Control-room review should decide how to normalize and promote:
1. Studio graph-vs-editor boundary
2. same-MOLT v1 bundle/merge restriction
3. NeoStack-scoped governance model
4. compiled sleeve file format boundary
5. one-active-sleeve workflow as product law

# BATCH-018 — ClawHub Skill Architecture Review

## Batch Overview
This batch reviews a chat that connected UMG architecture to a concrete ClawHub distribution path. It is strongest where it separates neutral packaging infrastructure from UMG runtime skills, clarifies MOLT block / NeoBlock / NeoStack / sleeve relationships, and pushes compiler doctrine away from hidden priority winner-picking toward explicit conflict detection and adjudication.

## Source Snapshot
- Source type: extracted chat summary
- Main focus: ClawHub skill ecosystem, UMG ontology refinement, compiler/runtime sequencing, release architecture
- Evidence status: evidence only, not canon
- Maturity note: several major concepts are high-value but still transitional, especially governance, priority doctrine, and final compiler implementation strategy

## Chat-Level Summary
The chat began with a ClawHub-facing skill architecture for UMG and gradually refined it into a layered runtime pipeline. A neutral builder/packager app was separated from UMG-specific skills. The conversation then deepened UMG ontology itself: MOLT blocks as atomic semantic units, NeoBlocks as locally coherent compiled assemblies, NeoStacks as domain-level assemblies of NeoBlocks, and sleeves as runtime identity containers. 

A major design shift occurred around compiler doctrine. The chat moved away from one rigid global priority order and toward a model of:
- conflict detection
- adjudication pass
- suppression of losers for the current compile
- recompilation

The conversation also strengthened distinctions between:
- bundle vs merge
- composition vs synthesis
- cognition/control vs rendering
- packaging infrastructure vs runtime cognition

## UMG-Relevant Extraction

### 1. Ecosystem architecture
- The app/tool should be neutral infrastructure for building and fixing skills.
- UMG is the advanced modular ecosystem built through that tool, not the tool itself.
- The runtime path should separate:
  - library loading
  - sleeve selection / resleeving
  - compilation / validation
  - output-envelope rendering

### 2. Ontology refinement
- MOLT block becomes the preferred atomic semantic term.
- NeoBlocks should be locally coherent, not globally exhaustive.
- NeoStacks should assemble multiple specialized NeoBlocks rather than overcompress into one giant unit.
- Sleeves remain the current runtime identity with defaults, constraints, governance-adjacent posture, and active stacks.

### 3. Structural distinctions
- Merge should be rare and synthesis-heavy.
- Bundle should remain the main grouping mechanism without identity loss.
- Overlay / adjacency / layering should not be collapsed into merge.
- Route activation should show what is in use now; structure shows what can exist.

### 4. Compiler/runtime redesign
- Pre-pass should become an explicit compiler phase.
- Priority should not be treated as a universal hard law.
- “No competition, no priority” became the strongest simplified working rule.
- Conflict detection plus Adjudication Pass replaced hidden winner-picking as the preferred direction.
- Renderer must remain downstream of resolved cognition/runtime state.

## Independent Review
This is one of the stronger architecture batches because it ties abstract UMG design directly to release structure and implementation sequencing. The strongest contribution is not any one skill name. It is the separation of concerns:
- neutral packaging infrastructure
- ontology/library layer
- runtime identity selection
- compilation/validation
- rendering

The batch also makes meaningful progress on internal UMG language. It narrows MOLT block, NeoBlock, NeoStack, merge, bundle, route, and overlay into a more legible system. The most important compiler implication is the move away from opaque automatic priority selection toward surfaced conflict and adjudication.

The main caution is that governance and final ontology are still not fully closed here. Some language is clearly mature enough to freeze as evidence, but not yet mature enough to treat as locked doctrine.

## Roadmap Mapping
- **Phase 1 — Core Alignment**
  - Clarifies MOLT block / NeoBlock / NeoStack / sleeve distinctions
  - Clarifies merge vs bundle vs overlay vs route
  - Clarifies “no competition, no priority” as a provisional operating principle
- **Phase 2 — Compiler Impact**
  - Strongly supports explicit pre-pass
  - Strongly supports conflict detection and Adjudication Pass
  - Strongly supports renderer-after-cognition ordering
- **Phase 3 — Documentation Impact**
  - Supports glossary, visual legend, route/state explanation, and product-positioning docs
- **Phase 4 — Skill Alignment**
  - Supports neutral builder/tool messaging
  - Supports library loader, sleeve selector, compiler, and renderer as distinct skills
- **Phase 5 — PRD and Staging**
  - Supplies release sequencing for neutral builder first, UMG runtime skills second

## Action Outcome
- Accept as evidence
- Export as Stage 1 pack
- Preserve as a central architecture-and-distribution batch
- Hold compiler doctrine as export-candidate language pending later canon lock

## Recommended Next Decision
Lock the ClawHub/UMG split and define a first formal compiler transition spec for:
1. explicit pre-pass,
2. conflict detection,
3. Adjudication Pass,
4. renderer-downstream ordering.

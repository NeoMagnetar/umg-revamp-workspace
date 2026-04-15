# BATCH-080_RAG_DYNAMIC_MERGE_REVIEW

## Batch Overview
- **Batch ID:** BATCH-080
- **Short Topic:** RAG Dynamic Merge
- **Review Status:** REVIEWED
- **Disposition:** ACCEPT_AS_EVIDENCE
- **Source Type:** Derived handoff summary, not raw transcript
- **Primary Domain:** runtime_architecture
- **Why this batch matters:** It extends UMG into retrieval-grounded runtime behavior by reframing RAG as a dynamic Merge-layer capability and by proposing an explicit `Retrieve -> Inject -> Render` execution path.

## Source Snapshot
- The source describes RAG as an AI architecture and then maps it into UMG using MOLT blocks.
- It proposes a UMG-compatible RAG loadout built from Primary, Subject, Philosophy, and Instruction roles.
- It treats RAG as a mid-pipeline augmentation layer and an evolution of Merge from static content to dynamic retrieval.
- It gives example Cantocore-like strings and example role assignments rather than a finalized compiler specification.
- The source is conceptual and architectural, not an implementation transcript or benchmarked runtime.

## Chat-Level Summary
This batch frames Retrieval-Augmented Generation as a modular extension to UMG rather than a separate external pattern. The main contribution is conceptual: Merge is no longer only static additive content, but can become a dynamic retrieval container that fetches external data at runtime and injects it before render. The source keeps UMG’s role structure intact—Primary, Subject, Philosophy, Instruction—while inserting RAG behavior into the execution layer through a truth-first philosophy and a retrieval-first instruction pipeline. The strongest value is runtime/compiler pressure, not finalized canon.

## UMG-Relevant Extraction
### Core semantics
- UMG remains a modular cognitive architecture built from composable blocks.
- Generation is described as **assembly + orchestration + rendering**.
- RAG is presented as a runtime augmentation mechanism that preserves modularity, traceability, and compositional control.

### Role/taxonomy pressure
- **Primary** activates a RAG mode, e.g. `RAG.ENABLED.MODULE`.
- **Subject** defines retrieval domain or knowledge space.
- **Philosophy** sets priority hierarchy such as `TRUTH > STYLE`.
- **Instruction** defines the execution pipeline, e.g. `RETRIEVE > INJECT > RENDER`.
- **Merge** is implicitly extended from static support content into a dynamic retrieval container.

### Runtime/compiler pressure
- Explicit flow proposed: **Retrieve -> Inject -> Render**.
- Runtime augmentation occurs at generation time rather than through precompiled static prompt assembly.
- Vector search and stackable memory are suggested runtime flags.
- RAG is positioned between instruction logic and final rendering.

### Documentation/product pressure
- Source uses a Cantocore / JSON-like loadout representation.
- Terminology includes `loadout`, `pipeline`, and `module`.
- Suggested future integrations point to vector DBs and RAG frameworks, implying SDK or engine-facing extension work.

## Independent Review
This batch is valuable because it creates a concrete bridge between UMG semantics and a familiar AI systems pattern. It does not merely say “UMG can use RAG”; it proposes where retrieval belongs in the modular stack and how role semantics constrain it. The strongest signal is that **Merge may need a split model**:
1. static merge content, and
2. dynamic retrieval-backed merge content.

That is a meaningful design pressure for the compiler/runtime, because it changes Merge from a text-combination operator into a possible execution hook.

At the same time, the source is still concept-level. It does not define ranking policy, source conflict resolution, context window management, fallback behavior, or whether RAG is a block type, a Merge mode, or a subsystem outside normal block taxonomy. Those unresolved boundaries should stay explicit.

## Roadmap Mapping
- **PHASE_1_CORE_ALIGNMENT**
  - Clarify whether RAG is a Merge extension, a distinct module, or both.
  - Clarify whether `Blueprint` remains outside retrieval or can shape retrieval behavior indirectly.
- **PHASE_2_COMPILER_IMPACT**
  - Define where `Retrieve -> Inject -> Render` enters the runtime pipeline.
  - Define retrieval hook behavior, source conflict handling, and token-budget controls.
- **PHASE_3_DOCUMENTATION_IMPACT**
  - Add dynamic Merge/RAG examples without implying canon prematurely.
  - Document truth-first behavior and retrieval-grounded generation as an optional extension.
- **PHASE_4_SKILL_ALIGNMENT**
  - Potential agent skills: retrieval-enabled Merge hooks, inspectable source injection, grounded output traces.
- **PHASE_5_PRD_AND_STAGING**
  - Candidate prototype: UMG-RAG demo with configurable retrieval settings and visible injection step.

## Action Outcome
- Accepted as evidence.
- Default four-file pack created.
- Optional extracts created only where the source clearly supported them:
  - compiler extract
  - blocks/MOLT extract
  - contradiction flags

## Recommended Next Decision
Determine whether RAG should be specified as:
1. a **dynamic Merge mode**,
2. a **distinct runtime subsystem**, or
3. a **dual model** where Merge can be either static or retrieval-backed.

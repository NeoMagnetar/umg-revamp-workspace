# BATCH-128 — Compiler v0 Overview Review

## Batch Overview
Batch ID: BATCH-128  
Source Type: derived summary / compiler-and-studio architecture consolidation, not a raw transcript  
Working Topic: compiler semantics, studio/editor separation, bundle-vs-merge-vs-NeoBlock distinction, independent compiler release path  
Review Status: REVIEWED  
Disposition: ACCEPT_AS_EVIDENCE

## Source Snapshot
The source is a structured summary titled `UMG Compiler v0 Overview`.
It consolidates a chat that moved between Replit runtime/debugging, UMG Studio UI architecture, compiler behavior auditing, mobile graph design, and release/interoperability strategy.
The strongest recurring topics are the distinction between authored Sleeve JSON, compiler-resolved artifacts, and UI/editor state; the separation between subset bundle/merge operations and whole-stack NeoBlock compression; the reassertion that priority does not change MOLT hierarchy; and the practical release stance that the compiler can ship independently of the unfinished UI.
Because this source is a derived summary rather than a raw transcript or direct code audit log, it should be treated as strong evidence of intended distinctions and practical findings, but not as automatic canon.

## Chat-Level Summary
This batch materially tightens the boundary between compiler truth and editor visualization.
Its most important semantic clarification is that bundle and merge act on selected blocks inside a stack, while compressing an entire stack into a NeoBlock is a separate stack-level operation.
The source also preserves a strong control rule: priority does not alter MOLT hierarchy, and governance remains the only override mechanism.
At the implementation level, the batch captures conversation-grounded findings about current compiler sequencing, deterministic behavior, prompt-oriented artifact generation, and the use of `sleeve.ui` metadata to preserve editor-only operations without contaminating compiler semantics.
It also records a release strategy that decouples compiler publication from Studio maturity, treating the UI as optional tooling rather than prerequisite infrastructure.

## UMG-Relevant Extraction
Sleeve JSON is treated as the authored source of truth.
The compiler reads authored structure and emits deterministic artifacts such as RuntimeSpec, Trace, and prompt-oriented derived outputs.
UI/editor visualization state remains distinct from both authored structure and compiler-resolved structure.
MOLT remains the canonical lane and taxonomy for stack composition.
Priority applies only within same-MOLT peer collisions and does not cross MOLT lanes or override governance.
Compiler audit findings summarized in the source include the presence of priorityGroup and priorityOrder on blocks, deterministic tie fallback by block id, governance-based priority overrides, and same-bucket priority resolution that preserves MOLT ordering.
Merge is described as an explicit subset operation inside a stack, using declared result blocks rather than inventing new runtime block ids.
Bundle is described as a subset grouping operation distinct from merge, with grouped selection behavior but no automatic creation of new compiler blocks.
Whole-stack compression into a NeoBlock is explicitly separate from subset bundle/merge behavior.
NeoBlocks are treated as stack-level artifacts that can be saved and placed into a higher-level graph.
NeoStacks are higher-level graph entities containing NeoBlocks and eventually other structures.
`sleeve.ui` and especially `sleeve.ui.ops` are used to preserve editor-only metadata without redefining sleeve semantics for the compiler.
Governance is repeatedly reinforced as the only override mechanism and is described as affecting eligibility and ordering without changing block content or crossing MOLT lanes.
A proposed idealized compiler flow appears as Validate → Scope → Governance → Merge → Priority → Synthesis, while a separate extracted summary of current compiler-v0 behavior lists compileSleeve, validation, normalizeSegments, applyMerges, applyBundles, applyGovernance, live filtering, resolveAuthority, per-type selection, buildNeoBlocks, buildNeoStacks, and artifact generation.
Prompt rendering is discussed as a separate official artifact direction via RuntimePromptSpec.

## Independent Review
This is a high-value semantic-boundary and implementation-clarification batch.
Its strongest contribution is not new theory alone, but the cleanup of confusing overlaps between editor interactions, subset operations inside a stack, whole-stack compression, and compiler law.
That distinction is highly important for both documentation and Studio design because it prevents UI affordances from silently becoming semantic claims.
The batch also helps stabilize the control model: priority is bounded to same-MOLT peer resolution, while governance remains the only override mechanism.
This is consistent with broader anti-drift goals inside the project.
The source is also useful because it carries practical migration signals: `client/` should not be treated as the canonical runtime, `apps/umg-studio` is the real UI, and the compiler can be independently published.
Main caution: because the source blends compiler audit summaries, UI design exploration, and runtime/release discussion, later synthesis should separate which parts are conversation-grounded implementation observations, which are proposed future directions, and which are already stable semantic candidates.

## Roadmap Mapping
Primary domain: compiler and studio boundary clarification with release-structure implications

Roadmap phases touched:
PHASE_1_CORE_ALIGNMENT
PHASE_2_COMPILER_IMPACT
PHASE_3_DOCUMENTATION_IMPACT
PHASE_4_SKILL_ALIGNMENT
PHASE_5_PRD_AND_STAGING
PHASE_6_GITHUB_EXECUTION

Key phase implications:
Phase 1: sharpens semantic boundaries among priority, governance, bundle, merge, NeoBlock compression, and JSON-as-specification.
Phase 2: suggests concrete compiler tasks around RuntimePromptSpec, hash outputs, deterministic failure documentation, and cleaner flow documentation.
Phase 3: provides strong candidate doc language for declarative specification, stack subset operations, and UI-versus-compiler separation.
Phase 4: carries workflow lessons for scoped agent prompting and file-targeted implementation instructions.
Phase 5: supports a graph-first Studio direction while preserving compiler independence.
Phase 6: records migration guidance around disabling dead-shell runtime paths and stabilizing the real app surface.

## Action Outcome
Accepted as evidence.
Frozen as a Stage 1 intake pack.
Optional compiler extract, canon candidates, and contradiction flags are justified because the batch contains dense compiler-facing distinctions, reusable documentation language, and explicit ambiguity/risk surfaces around priority, UI drift, and runtime targeting.

## Recommended Next Decision
Control-room review should decide how to normalize and promote the following boundaries:
1. subset bundle/merge inside a stack vs whole-stack NeoBlock compression
2. priority language vs governance language in docs and UI
3. RuntimePromptSpec and hash/integrity artifact status
4. Studio runtime migration away from dead-shell paths

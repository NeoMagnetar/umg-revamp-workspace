# BATCH-126 — Compiler Glossary Review

## Batch Overview
Batch ID: BATCH-126  
Source Type: derived summary / glossary-style consolidation, not a raw transcript  
Working Topic: compiler structure, block hierarchy, priority model, bundle vs merge, UI/compiler boundary  
Review Status: REVIEWED  
Disposition: ACCEPT_AS_EVIDENCE

## Source Snapshot
The source is a structured summary titled `UMG Compiler Glossary`.
It consolidates conceptual work around UMG structural units and compiler semantics, including Blocks, Columns / MOLT Columns / cocoons, NeoBlocks, NeoStacks, Sleeves, Governance, Priority, Trigger behavior, Merge, Bundle, compiler pipeline, UI semantics, and repo/workflow guidance.
It also records a terminology shift away from `stack_rank` toward `priority_group`.
Because this source is a polished derived summary rather than a raw chat transcript or locked canonical spec, it should be treated as strong evidence of design direction rather than automatic canon.

## Chat-Level Summary
This batch materially clarifies the modern structural picture of UMG.
Its main moves are:
1. separate structural composition from authority
2. replace numeric rank-like semantics with categorical priority groups
3. distinguish bundle, merge, synthesis, and attachment scope
4. define clearer structural layers from Block → Column → NeoBlock → NeoStack → Sleeve
5. preserve compiler determinism by forcing UI actions to emit explicit metadata rather than implicit meaning

The batch also reinforces that the compiler must remain deterministic, non-inferential, model-agnostic, and audit-oriented, with RuntimeSpec and Trace as its outputs.
It is particularly valuable because it bridges conceptual semantics, compiler staging, UI design implications, and repo/workflow guidance in one compact source.

## UMG-Relevant Extraction
Everything in UMG is ultimately a modular block, with some larger structures being compressed assemblies of smaller ones.
The source keeps structure, authority, combination, and rendering distinct.
MOLT is treated here as the fixed hierarchy of authority, with the stated order Trigger, Directive, Instruction, Subject, Primary, Philosophy, Blueprint.
Priority does not override MOLT and is only used among peers in the same scope and resolution context.
`stack_rank` is explicitly rejected and replaced with `priority_group`.
Priority is categorical rather than numeric, with named groups such as critical, high, normal, low, and experimental.
Bundle and merge are sharply distinguished:
- bundle keeps multiple contributions active and orders influence
- merge resolves multiple contributions into one outcome when required
Merge across MOLT areas is allowed only as structured runtime assembly or explicit typed derivation, not as untyped blob fusion.
NeoBlock is defined as a compressed representation of one Column and should expose one MOLT type upward in v0.
NeoStack is a grouping of snapped sibling NeoBlocks and is not itself authority or precedence.
NeoStacks may run in bundle or merge mode, but the default remains unresolved.
Sleeve is the top-level organism and compiler input.
Governance is treated as explicit, scoped, traceable, useful, but not always required.
The compiler input is Sleeve and the outputs are RuntimeSpec plus Trace.
The compiler pipeline is described as validate, normalize, off/disabled handling, apply attachments, resolve bundle or merge behavior, enforce MOLT authority, run explicit synthesis, build RuntimeSpec, canonicalize and hash, then emit final Trace.
UI zoom levels are treated as view transformations rather than semantic changes.
UI gestures should generate explicit metadata rather than hidden meaning.
Documentation and schema work are treated as required before heavy implementation.

## Independent Review
This is a high-value Stage 1 batch for semantic stabilization because it tightens multiple ambiguity-prone areas at once.
The strongest signal is the refactor away from `stack_rank` into `priority_group`, which helps decouple authority from ranking-style intuition and reduces the risk of accidental hidden precedence.
The source is also valuable for drawing a usable visual/structural ladder from Blocks to Sleeves without letting UI compression or snapping mutate semantics.
Another major strength is that it keeps the compiler intentionally non-agentic: no guessing, no inference, no ambient propagation, no hidden optimization.
Caution is still warranted in three places.
First, the source presents MOLT as authority in a stronger way than some other evidence sources that frame MOLT as semantic ordering while governance performs override; this should be cross-compared later.
Second, NeoStack default compose mode remains unresolved.
Third, governance semantics remain partly unsettled around capstone vs overlay behavior, scope, and defer/off/apply modes.
Overall, this batch should be preserved as strong evidence, not promoted automatically.

## Roadmap Mapping
Primary domain: core semantics with direct compiler, documentation, and staging impact

Roadmap phases touched:
PHASE_1_CORE_ALIGNMENT
PHASE_2_COMPILER_IMPACT
PHASE_3_DOCUMENTATION_IMPACT
PHASE_4_SKILL_ALIGNMENT
PHASE_5_PRD_AND_STAGING
PHASE_6_GITHUB_EXECUTION

Key phase implications:
Phase 1: sharpens structural model, priority semantics, and bundle/merge distinctions.
Phase 2: implies concrete compiler work for priority groups, canonicalization, attachment resolution, MergeOps, and trace structure.
Phase 3: supplies plain-language documentation candidates and glossary material.
Phase 4: affects any skill or builder logic that currently assumes implicit precedence from position or snapping.
Phase 5: supports pre-code schema and staging decisions.
Phase 6: provides repo split and workflow guidance for compiler vs Studio.

## Action Outcome
Accepted as evidence.
Frozen as a Stage 1 intake pack.
Optional compiler extract, canon candidates, and contradiction flags are justified because the source is dense with compiler rules, candidate laws, and open tensions.

## Recommended Next Decision
Control-room review should compare this batch against existing evidence on:
1. whether MOLT is semantic ordering only or a true authority system
2. whether governance is optional overlay or sole override mechanism
3. whether NeoStack default should be bundle or merge
4. whether `priority_group` is ready for promotion as the stable successor to `stack_rank`

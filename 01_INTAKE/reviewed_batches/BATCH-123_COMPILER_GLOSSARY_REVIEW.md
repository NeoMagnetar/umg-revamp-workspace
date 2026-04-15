# BATCH-123 — Compiler Glossary / Specification Review

## Batch Overview
Batch ID: BATCH-123  
Source Type: derived specification / glossary text, not a raw transcript  
Working Topic: compiler glossary, canonical terminology, semantic ordering, governance boundaries  
Review Status: REVIEWED  
Disposition: ACCEPT_AS_EVIDENCE

## Source Snapshot
The source is a structured specification-style text titled `UMG — Canonical Glossary (v0, Locked)`.
It presents declarative definitions for UMG, CSL, MOLT, blocks, MOLT type order, Molt Stack, bundles, merges, roles, Off state, Snap, Scope, Synthesis, NeoBlock, NeoStack, Governance, Sleeve, Compiler, RuntimeSpec, Trace, and Determinism.
The source explicitly frames itself as compiler-accurate, terminology-stable, and aligned with original intent.
Because this is a derived specification artifact rather than a raw conversation transcript, its statements are strong evidence of intended semantics but still require later control-room confirmation before promotion into canon.

## Chat-Level Summary
This batch captures a highly consolidated semantic specification for UMG.
Its main stabilizing move is the separation of semantic ordering from conflict resolution:
MOLT hierarchy establishes framing order, while governance alone performs override, suppression, disabling, or deterministic tie-breaking.
The text also clarifies that bundles preserve structure without synthesis, merges are explicit synthetic operations requiring a result block, Off is a state or role rather than a MOLT type, and Trace is mandatory for UMG validity.
The batch is unusually useful because it compresses a large number of prior ambiguity-prone concepts into short, compiler-facing rules.

## UMG-Relevant Extraction
UMG is defined as a Cognitive Specification Layer rather than an execution system.
MOLT is defined as typed grammar concerned with semantic position, legal interaction, and compilation constraints rather than behavior itself.
The canonical MOLT order is Trigger, Directive, Instruction, Subject, Primary, Philosophy, Blueprint.
That order is semantic precedence only, not automatic suppression.
Blocks are atomic, typed, inert outside a sleeve, and never implicitly modified or removed.
Molt Stack is the canonical term for a vertical ordered composition unit; compiler term remains Stack.
Horizontal alignment creates peer standing within a type but does not guarantee identical outcome.
Bundle is grouping without semantic alteration.
Merge is explicit synthesis that creates a new block and preserves source traceability.
Role is independent from type; canonical roles listed are PrimaryShell, MergeContributor, BlueprintGuide, and Off.
Off excludes a block from compilation while preserving it for later reactivation.
Snap is UI-only and has no compiler semantics.
Scope is the explicit compiler-evaluated set and is independent of UI layout.
NeoBlock is the compiled representation of one resolved Molt Stack.
NeoStack is a domain-level grouping of NeoBlocks and has no intrinsic authority.
Governance is the only layer allowed to override, disable, redirect, enforce limits, or break ties.
Sleeve is a static cognitive design container with no execution or state.
Compiler is the deterministic transformer that emits RuntimeSpec and Trace.
Trace is mandatory; the source states that “No Trace = not UMG.”
Determinism requires stable ordering, explicit rules, and no hidden randomness.

## Independent Review
This is one of the strongest Stage 1 evidence batches so far for semantic stabilization.
Its value is not novelty alone but compression: it collapses recurring ambiguities into crisp distinctions that appear directly actionable for later compiler and documentation alignment.
The most important clarification is the de-overloading of “authority.”
By splitting hierarchy into semantic ordering and governance into conflict resolution, the text provides a viable route for resolving prior confusion around override, suppression, OFF behavior, and equal-level interaction.
The source also materially helps documentation because many definitions are written in release-friendly, user-facing language already.
Main caution: the source is a polished specification artifact. That makes it strong evidence of intended semantics, but it also means later synthesis should still verify compatibility with existing compiler behavior, documentation wording, and previously reviewed batches before canon lock.

## Roadmap Mapping
Primary domain: core semantics with direct compiler and documentation impact

Roadmap phases touched:
PHASE_1_CORE_ALIGNMENT
PHASE_2_COMPILER_IMPACT
PHASE_3_DOCUMENTATION_IMPACT
PHASE_4_SKILL_ALIGNMENT
PHASE_5_PRD_AND_STAGING

Key phase implications:
Phase 1: strong candidate definitions for MOLT order, governance boundary, Off semantics, bundle vs merge, and NeoBlock / NeoStack positioning.
Phase 2: implies parser, normalization, trace, suppression, and scope evaluation rules that should be tested against compiler behavior.
Phase 3: offers near-ready glossary language and terminology normalization targets.
Phase 4: affects any skill that currently treats hierarchy as suppression or conflates type with role.
Phase 5: provides PRD-grade baseline language for system purpose, outputs, and determinism.

## Action Outcome
Accepted as evidence.
Frozen as a Stage 1 intake pack.
Optional compiler extract and canon-candidate extract are justified because the source is specification-dense and explicitly presents locked terminology, but no canon promotion is performed here.

## Recommended Next Decision
Control-room review should test whether the claimed canonical distinctions fully align with already reviewed evidence around:
1. trigger semantics
2. governance vs hierarchy behavior
3. Off participation rules
4. bundle vs merge trace behavior
5. NeoBlock / NeoStack downstream routing semantics

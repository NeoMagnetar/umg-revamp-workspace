# BATCH-130 — Branch · Branch · Block Stack Framework Review

## Batch Overview
Batch ID: BATCH-130  
Source Type: derived summary / compiler-spec consolidation, not a raw transcript  
Working Topic: compiler glossary stabilization, bundle vs merge, governance, trigger schema, pipeline, RuntimeSpec/Trace, PRD outline  
Review Status: REVIEWED  
Disposition: ACCEPT_AS_EVIDENCE

## Source Snapshot
The source is a structured consolidation titled `Branch · Branch · Block Stack Framework`.
It summarizes a chat focused on formalizing UMG compiler concepts and tightening the meanings and relationships of Block, MOLT, Bundle, Merge, NeoBlock, NeoStack, Sleeve, Governance, Trigger, Priority, RuntimeSpec, and Trace.
The discussion moved from conceptual terminology refinement into implementation planning, including compiler pipeline stages, trigger/governance schemas, RuntimeSpec/Trace shapes, error codes, and a PRD outline.
Because the source is a derived summary rather than a raw transcript or direct code diff, it should be treated as strong evidence of intended semantics and implementation direction, but not as automatic canon.

## Chat-Level Summary
This batch is one of the strongest compiler-facing Stage 1 evidence sources in the current run.
Its central contribution is semantic stabilization at the exact boundary where terminology must serve theory, compiler behavior, and UI communication simultaneously.
The batch repeatedly sharpens distinctions among authority, priority, governance, directive, merge, bundle, and visual grouping.
It also proposes a near-implementation-ready deterministic compile pipeline, explicit trigger/governance models, RuntimeSpec and Trace schema directions, and a phased PRD outline.
The result is not final canon, but it is unusually dense with language and structures that later synthesis can likely mine directly.

## UMG-Relevant Extraction
UMG is framed as a Cognitive Specification Layer that specifies cognition but does not execute it.
RuntimeSpec and Trace are treated as mandatory outputs, with the rule “No Trace = not UMG.”
Canonical MOLT order is stabilized as Trigger, Directive, Instruction, Subject, Primary, Philosophy, Blueprint.
MOLT type and role are explicitly separated.
Off is retained as a role/state rather than a MOLT type.
Governance is explicitly not a MOLT type.
Triggers are simplified in v0 so active trigger IDs are passed into the compiler externally rather than computed by the compiler.
Priority is separated from authority: authority determines who may override, while priority determines ordering within an allowed level.
“Stack rank” is rejected in favor of “priorityOrder.”
Bundle becomes the canonical term for ordered grouping without new meaning.
Merge becomes the canonical term for explicit construction of a new semantic unit with preserved lineage.
Merge is placed under the broader umbrella of synthesis, but is not identical to synthesis.
Compiler-facing segment logic becomes important: bundle segments and merge segments are the semantic compilation units.
NeoBlock is treated as a compressed result that may contain bundles, merged pieces, singleton items, and structured internals.
NeoStack is treated as a canonical domain-level grouping of blocks or NeoBlocks with peer authority rather than implicit precedence.
Governance is described as a law/control layer that can forbid, require, prefer, limit, or override priority through explicit rules and bindings.
The compiler is locked as deterministic, rule-enforcing, non-agentic, and non-AI-calling.
An 11-step pipeline is proposed from validation through final Trace/result.
RuntimeSpec and Trace schema directions are explicitly detailed, including event types and error taxonomy.
A phased compiler PRD outline is created.

## Independent Review
This batch has unusually high Stage 1 value because it does not just repeat abstract positioning; it translates semantic distinctions into implementation surfaces.
The strongest contribution is the stabilization of language at the exact points most likely to create future drift:
authority vs priority,
merge vs bundle,
governance vs directive,
semantic structure vs UI grouping,
compiler determinism vs later AI-assisted authoring or runtime help.
The move to treat the compiler as seeing segments rather than loose stacked blocks is especially significant because it compresses multiple ambiguous UI states into a cleaner compile model.
The source also has substantial documentation value because it explicitly demotes or rejects confusing terms such as stack rank, union, overlay, compound, integrate, and head block.
Main caution: some points remain only near-locked rather than fully locked, especially around Primary merge, Trigger merge, implicit singleton bundles, and NeoBlock entry paths.
Later control-room synthesis should preserve those unresolved tensions rather than flattening them into false certainty.

## Roadmap Mapping
Primary domain: compiler semantics and implementation-ready language stabilization

Roadmap phases touched:
PHASE_1_CORE_ALIGNMENT
PHASE_2_COMPILER_IMPACT
PHASE_3_DOCUMENTATION_IMPACT
PHASE_4_SKILL_ALIGNMENT
PHASE_5_PRD_AND_STAGING
PHASE_6_GITHUB_EXECUTION

Key phase implications:
Phase 1: strong candidate clarifications for MOLT order, Off semantics, governance separation, authority vs priority, and bundle vs merge law.
Phase 2: near-direct compiler planning signal for trigger handling, governance bindings, segment normalization, NeoBlock/NeoStack construction, error taxonomy, and Trace events.
Phase 3: gives documentation-ready canonical and rejected term lists, along with usable explanatory mappings between UI language and compiler language.
Phase 4: affects any skill or assistant behavior that currently conflates governance with directive, merge with grouping, or authority with ranking.
Phase 5: provides PRD-grade structure through compiler goals, non-goals, phases, and acceptance-minded design.
Phase 6: informs future repo/spec partitioning and implementation sequence.

## Action Outcome
Accepted as evidence.
Frozen as a Stage 1 intake pack.
Optional compiler extract, canon candidates, and contradiction flags are justified because the batch contains implementation-facing rules, schema directions, PRD-level planning, and several unresolved tensions that need explicit preservation.

## Recommended Next Decision
Control-room review should decide how to normalize and promote:
1. segment-first compiler model
2. authority vs priority law
3. bundle vs merge vs UI collapse terminology
4. governance binding model
5. trigger v0 input model

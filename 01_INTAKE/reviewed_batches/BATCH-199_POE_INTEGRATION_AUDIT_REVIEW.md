# BATCH-199 — Poe Integration Audit — Review

## Batch Overview
- **Batch ID:** BATCH-199
- **Source Type:** derived branch summary / canon-building and compiler-planning batch
- **Review Status:** REVIEWED
- **Disposition:** ACCEPT_AS_EVIDENCE
- **Primary Domain:** canon_compiler_alignment
- **Evidence Strength:** high
- **Why it matters:** this batch locks major positioning language for UMG, establishes a detailed compiler plan, freezes a documentation sequence, clarifies stack/snap/merge/sleeve semantics, and strongly reinforces UMG as a tech-agnostic Cognitive Specification Layer.

## Source Snapshot
- The source summarizes a substantial branch focused on canon stabilization, compiler planning, documentation sequencing, terminology locking, and repo strategy.
- It covers:
  - UMG as a tech-agnostic Cognitive Specification Layer (CSL)
  - MOLT type locking and authority order
  - Trigger restrictions
  - stack and merge mechanics
  - sleeve and compilation semantics
  - RuntimeSpec + Trace as canonical outputs
  - documentation structure categories 0–9
  - greenfield compiler and repo plan
- The source is a secondary synthesis of a long working branch, not a single raw transcript artifact.

## Chat-Level Summary
This batch is one of the strongest Stage 1 evidence sources for core UMG stabilization. Its main contribution is not novelty but **formal locking pressure**: it repeatedly fixes terminology, freezes ordering, draws lines between canon and extensions, and describes a deterministic compiler pipeline that turns static sleeve content into RuntimeSpec + Trace. It also resolves several tensions, especially around Merge no longer being a MOLT type, Trigger restrictions, and UMG as a specification layer rather than an agent/runtime/orchestrator.

## UMG-Relevant Extraction
### Core Semantics
- UMG is repeatedly locked as a **tech-agnostic Cognitive Specification Layer (CSL)**.
- UMG specifies cognition rather than executing cognition.
- UMG is separated from models, prompts, orchestration, tools, and stateful agents.
- UMG's primary canonical outputs are RuntimeSpec + Trace.
- UMG is described as structured, modular, deterministic, and auditable cognition.

### Roles / Taxonomy
- Canonical MOLT types repeatedly fixed as:
  - Trigger
  - Directive
  - Instruction
  - Subject
  - Primary
  - Philosophy
  - Blueprint
  - Off
- Merge is removed as a MOLT type and treated as an operation.
- Roles are treated separately from MOLT type, with recurring role language:
  - PrimaryShell
  - MergeContributor
  - BlueprintGuide
  - Off
- “MOLT Primary != Role PrimaryShell” is explicitly locked.

### Runtime / Compiler
- Input/output contract:
  - input = Sleeve JSON
  - output = RuntimeSpec + Trace
- Fixed compiler pipeline repeatedly stated:
  - parse
  - validate
  - choose snap
  - select snap blocks
  - remove Off blocks
  - resolve stacks
  - apply triggers
  - enforce authority/directionality
  - merge
  - validate PrimaryShell
  - emit RuntimeSpec
  - emit Trace
- Determinism is mandatory.
- Trace is mandatory and chronological.
- RuntimeSpec is execution-neutral and not itself a prompt.

### Governance / Control
- Drift prevention is central.
- Canon governance is enforced through:
  - glossary authority
  - fixed doc sequence
  - versioning
  - explicit non-canon extension handling
- No silent redefinition or synonym creep is allowed.
- Experimental material must live outside canon.

### Structural Composition
- Block = atomic unit of cognition.
- Sleeve = static, inert container of potential cognition.
- Stack = strict compiler-level same-type priority resolution.
- Domain emerges as the strongest candidate human-facing term for cross-type conceptual grouping.
- Snap semantics are refined toward scope/membership rather than overloaded grouping/merge behavior.

## Independent Review
This batch is one of the clearest foundation-level evidence sources in the current intake set. It is especially important because it supplies:
- a strong top-level definition of what UMG is
- explicit compiler contract language
- fixed authority and MOLT ordering
- governance against canon drift
- a documented sequence for stable writing and implementation

Its main limitations:
- it is still a branch synthesis rather than a finalized canonical release
- terminology around stack vs domain/profile/bundle remains the main unresolved tension
- UI graph mechanics remain conceptually rich but not fully canonized
- some repo migration details are still strategic rather than implemented

This should therefore be treated as **high-value evidence** for alignment, compiler design, and doc structure, but not as automatic canon by itself.

## Roadmap Mapping
- **PHASE_1_CORE_ALIGNMENT:** CSL positioning, MOLT types, authority order, glossary hierarchy, canon governance
- **PHASE_2_COMPILER_IMPACT:** pipeline, Trace/RuntimeSpec contract, trigger actions, stack/merge law
- **PHASE_3_DOCUMENTATION_IMPACT:** categories 0–9 doc structure, sequence control, glossary primacy
- **PHASE_4_SKILL_ALIGNMENT:** AGENTS.md guidance, agent-usable structured consumption, Replit workflow
- **PHASE_5_PRD_AND_STAGING:** fresh repo strategy, milestone plan, staged compiler implementation

## Action Outcome
- Accepted as evidence.
- Default four-file pack created.
- Optional extracts created only for:
  - compiler/runtime pressure
  - blocks/MOLT taxonomy pressure
  - neostructure / layered composition pressure
  - contradiction / ambiguity tracking

## Recommended Next Decision
Decide whether “Domain” should be formally locked as the human-facing term for cross-type grouped cognition, or whether further naming review is still required before canon freezing.

# BATCH-175 — CSL Canon and Compiler Foundations Review

## Batch Overview
Batch ID: BATCH-175  
Source Type: derived summary / canon-building and implementation-planning consolidation  
Working Topic: UMG as CSL, MOLT taxonomy, compiler pipeline, documentation sequence, repo strategy, terminology stabilization  
Review Status: REVIEWED  
Disposition: ACCEPT_AS_EVIDENCE

## Source Snapshot
The source captures a large canon-building and implementation-planning session that moved from broad UMG framing into structured stabilization work. Its strongest recurring themes are:
- UMG as a tech-agnostic Cognitive Specification Layer (CSL)
- separation of CSL from compiler and runtime execution
- fixed MOLT taxonomy and authority order
- formal compiler pipeline and artifacts
- canonical documentation sequence
- greenfield `umg-core` repo strategy
- drift prevention and canon governance

## Chat-Level Summary
This batch is strongest as a canon-foundation and compiler-foundation source. Its central contribution is a clear reframing of UMG away from agent/runtime confusion and toward a precise definition: UMG is a tech-agnostic Cognitive Specification Layer that specifies cognition structurally and deterministically rather than executing it.

The second strongest contribution is the compiler contract. The source repeatedly defines UMG input/output and the stages by which authored cognition becomes RuntimeSpec plus Trace.

The third strongest contribution is governance against drift through glossary authority, frozen documentation order, explicit versioning, and no silent synonym creep.

## UMG-Relevant Extraction
The source repeatedly locks UMG as a **tech-agnostic Cognitive Specification Layer (CSL)**.
UMG is described as:
- specifying cognition rather than executing it
- producing `RuntimeSpec + Trace`
- technology-agnostic and model-agnostic
- suitable across planners, chatbots, policy systems, and structured cognition

MOLT taxonomy is repeatedly stabilized as:
- Trigger
- Directive
- Instruction
- Subject
- Primary
- Philosophy
- Blueprint
- Off

A major refinement is that **Merge is removed as a MOLT type** and treated as an operation instead.
Role/type separation is explicit:
- `PrimaryShell`
- `MergeContributor`
- `BlueprintGuide`
- `Off`

Authority order is repeatedly fixed as:
Trigger > Directive > Instruction > Subject > Primary > Philosophy > Blueprint > Off

Trigger is defined as highest-authority activation/control logic. For compiler v0 it is simplified to actions-only with no condition evaluation.
Allowed actions repeatedly listed in the source:
- `enable_blocks`
- `disable_blocks`
- `set_directive_params`
- `request_tool`
- `set_merge_mode`

Priority is formalized at two levels:
- cross-type authority through fixed MOLT order
- same-type conflict resolution through stack/key/rank logic

Merge is formalized as an operation:
- same MOLT type
- same non-empty merge_key
- explicit policies such as strict, append, dedupe_append, compose_fields, prefer_higher_rank

Blocks are repeatedly defined as:
- atomic units of cognition
- one idea / one rule / one value / one constraint
- typed by one MOLT type
- inert until compiled

Sleeves are repeatedly defined as:
- static, lifeless containers of potential cognition
- holding blocks, snaps, defaults, domains, metadata
- not agents
- not runtime state

Blueprint/render separation is strong:
- Blueprint is silent structure/style influence only
- RuntimeSpec is not a prompt
- output formatting/rendering is downstream from canonical cognition structure

Compiler pipeline is one of the strongest preserved signals:
parse → validate → choose snap → select snap blocks → remove Off → resolve stacks → apply triggers → enforce authority/directionality → merge → validate PrimaryShell → emit RuntimeSpec → emit Trace

Documentation architecture is also frozen in a highly structured way:
0 Entry & Orientation
1 White Paper
2 Canonical Glossary
3 MOLT & Cognition Mechanics
4 Structural Composition
5 Conflict Resolution Mechanics
6 Sleeve & Compilation
7 Versioning & Governance
8 Examples & Applications
9 Future / Non-Canon Extensions

## Independent Review
This is one of the strongest Stage 1 canon-foundation sources in the intake corpus. It ties together terminology, compiler behavior, documentation order, and governance process.

## Roadmap Mapping
Primary domain: canon semantics, compiler contract, and documentation/governance stabilization

Roadmap phases touched:
PHASE_1_CORE_ALIGNMENT
PHASE_2_COMPILER_IMPACT
PHASE_3_DOCUMENTATION_IMPACT
PHASE_4_SKILL_ALIGNMENT
PHASE_5_PRD_AND_STAGING
PHASE_6_GITHUB_EXECUTION
PHASE_7_RELEASE_READINESS

## Action Outcome
Accepted as evidence.
Frozen as a Stage 1 intake pack.
Optional compiler extract, sleeve extract, blocks/MOLT extract, canon candidates, and contradiction flags are justified because the source contains foundational semantic law, a strong compiler pipeline, role taxonomy, sleeve doctrine, and unresolved naming tensions.

## Recommended Next Decision
Control-room review should decide how to normalize and promote:
1. CSL positioning as top-level canon language
2. final canonical human-facing term for cross-type grouping
3. compiler v0 pipeline as formal implementation contract
4. glossary/document-order governance as canon process law
5. exact relationship between role language and MOLT type language

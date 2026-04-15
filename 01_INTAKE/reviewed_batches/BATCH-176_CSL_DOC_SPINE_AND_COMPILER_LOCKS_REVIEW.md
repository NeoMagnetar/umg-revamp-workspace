# BATCH-176 — CSL Doc Spine and Compiler Locks Review

## Batch Overview
Batch ID: BATCH-176  
Source Type: derived summary / canonical language, compiler model, and documentation-structure consolidation  
Working Topic: CSL identity, MOLT taxonomy, compiler pipeline, canonical docs 0–9, terminology correction, implementation readiness  
Review Status: REVIEWED  
Disposition: ACCEPT_AS_EVIDENCE

## Source Snapshot
The source captures another major canon-building session focused on refining UMG’s vocabulary, compiler model, and documentation order.
Its strongest recurring themes are:
- UMG as a tech-agnostic Cognitive Specification Layer
- human-legible and machine-enforceable cognition specification
- fixed canonical MOLT taxonomy and authority order
- compiler-safe distinctions between stack, merge, snap, and domain
- full documentation spine across categories 0–9
- deterministic compiler implementation planning
- strict correction of terminology drift and sequence drift

The source is especially valuable because it combines nearly complete documentation language with implementation-facing compiler decisions, while also preserving the central unresolved naming tensions.

## Chat-Level Summary
This batch is strongest as a canon-spine and compiler-lock source.
Its central contribution is not merely defining UMG again, but tightening the entire conceptual skeleton:
what UMG is,
what it is not,
how it should be documented,
how it should compile,
and which terms must stop drifting.

The strongest reusable signal is the repeated lock:
UMG is a tech-agnostic Cognitive Specification Layer.
It specifies cognition, not execution.
It is not a model, runtime, agent, orchestration framework, or prompt library.

The second strongest contribution is the documentation spine and sequencing discipline.
The source treats document order as a structural anti-drift mechanism, not just a writing convenience.

The third strongest contribution is the compiler boundary work:
input/output contract,
pipeline ordering,
Trace requirements,
determinism,
and the separation between structural compiler operations and broader human-facing conceptual groupings.

## UMG-Relevant Extraction
The source repeatedly locks UMG as a tech-agnostic **Cognitive Specification Layer (CSL)**.
UMG is described as:
- specifying cognition, not execution
- a human-legible, machine-enforceable cognitive specification language
- a contract/constitutional layer between human intent and downstream execution
- deterministic, transparent, and auditable by design

Canonical MOLT types are repeatedly stabilized as:
- Trigger
- Directive
- Instruction
- Subject
- Primary
- Philosophy
- Blueprint
- Off

Merge is explicitly removed from canonical compiler MOLT types and treated as an operation.
Roles remain orthogonal to MOLT type, with repeated role references such as:
- PrimaryShell
- MergeContributor
- BlueprintGuide
- Off

PrimaryShell is explicitly locked as exactly one per active snap.

Authority order is again fixed as:
Trigger > Directive > Instruction > Subject > Primary > Philosophy > Blueprint > Off

Trigger is highest authority and compiler-state-facing.
Its v0 purpose is limited to:
- enable blocks
- disable blocks
- set directive parameters
- request tools
- set merge mode

Trigger must not:
- rewrite content
- create blocks
- bypass trace
- evaluate conditions in v0

Priority/authority is framed as:
- fixed global non-configurable authority order
- inward influence toward PrimaryShell
- lower-authority blocks may not override higher-authority blocks

Merge is again defined as same-type, keyed, policy-driven combination.
Same-type stack resolution and same-type merge remain distinct:
- stack = choose one among competing same-type blocks
- merge = combine compatible same-type blocks

A significant conceptual refinement appears in the distinction between:
- structural merge / compiler merge
- creative synthesis / cross-domain melding
This indicates awareness that older broader UMG meaning for merge may not be fully preserved by compiler canon.

The source repeatedly explores human-facing grouping language beyond mechanical stack.
Domain emerges again as the strongest candidate term, while profile/preset/bundle remain nearby alternatives.
This is tied directly to the unresolved tension between:
- original broader “stack” meaning
- narrowed compiler-safe “stack” meaning

Blocks are repeatedly defined as:
- singular atomic units of thought
- one idea / one value / one rule / one constraint
- inert and declarative until compiled
- split when concerns become separable

Sleeves are repeatedly defined as:
- lifeless, static containers of potential cognition
- holding blocks, domains, snaps, defaults, metadata
- not agents, runtimes, or memory

Blueprint remains structure/style only.
BlueprintGuide must remain silent.
RuntimeSpec is repeatedly defined as not a prompt.
Prompt rendering and execution remain downstream from canon.

Compiler contract is highly explicit:
input = Sleeve JSON
outputs = RuntimeSpec + Trace

Pipeline repeatedly locked:
1. parse sleeve
2. validate sleeve
3. choose snap
4. select snap blocks
5. remove Off blocks
6. resolve stacks
7. apply triggers
8. apply hierarchy / directionality
9. merge same-type groups
10. validate PrimaryShell exactly one
11. emit RuntimeSpec + Trace

Determinism is mandatory.
No Trace = not UMG-compliant is repeated as a strong compliance formulation.

Documentation spine is near-complete and repeated in stable form:
0.1 README.md
0.2 QUICKSTART.md
1.1 WHITE_PAPER.md
1.2 UMG as a Cognitive Specification Layer
2.1 GLOSSARY.md
3.1 MOLT_OVERVIEW.md
3.2 MOLT_TYPES.md
3.3 AUTHORITY_AND_DIRECTIONALITY.md
4.1 BLOCKS.md
4.2 DOMAINS.md
4.3 SNAP_AND_SCOPE.md
5.1 STACKING.md
5.2 MERGE.md
6.1 SLEEVE.md
6.2 COMPILER.md
6.3 RUNTIMESPEC.md
6.4 TRACE.md
7.1 VERSIONING.md
7.2 CANON_GOVERNANCE.md
8.1 EXAMPLES.md
8.2 UMG_VS_OTHER_SYSTEMS.md
9.1 EXTENSIONS.md

## Independent Review
This is one of the stronger Stage 1 canon-foundation batches because it reinforces not only the CSL positioning and compiler contract, but also the writing discipline required to keep the canon coherent.
The strongest value is the integrated pairing of:
semantic law,
compiler law,
documentation order,
and drift-prevention process.

The largest unresolved tension remains the naming problem:
stack in its original broader UMG sense versus stack in narrow compiler arbitration language, plus the related problem of what human-facing label should describe cross-type coherent groupings.

The source is particularly useful because it surfaces that tension explicitly instead of hiding it.

## Roadmap Mapping
Primary domain: canon documentation spine, compiler contract, and terminology stabilization

Roadmap phases touched:
PHASE_1_CORE_ALIGNMENT
PHASE_2_COMPILER_IMPACT
PHASE_3_DOCUMENTATION_IMPACT
PHASE_4_SKILL_ALIGNMENT
PHASE_5_PRD_AND_STAGING
PHASE_6_GITHUB_EXECUTION
PHASE_7_RELEASE_READINESS

Key phase implications:
Phase 1: strengthens CSL identity, MOLT order, authority, and block/sleeve semantics.
Phase 2: provides implementation-ready compiler contract and pre-coding decision list.
Phase 3: reinforces exact document order and glossary-first governance.
Phase 4: informs coding-agent workflow and file-by-file build discipline.
Phase 5: sharpens docs-first and compiler-next staging.
Phase 6: supports clean `umg-core` repo strategy and TypeScript/Vitest implementation path.
Phase 7: improves release readiness by locking semantics before community-facing rollout.

## Action Outcome
Accepted as evidence.
Frozen as a Stage 1 intake pack.
Optional compiler extract, sleeve extract, blocks/MOLT extract, canon candidates, and contradiction flags are justified because the source contains strong canon-facing law, compiler model details, sleeve doctrine, and unresolved naming tensions that require explicit tracking.

## Recommended Next Decision
Control-room review should decide how to normalize and promote:
1. CSL language as top-level identity canon
2. final naming for cross-type conceptual grouping
3. whether “stack” should remain compiler-arbitration terminology or be renamed
4. compiler v0 contract and strictness decisions before coding
5. migration language for older repo/docs that still use older merge/stack semantics

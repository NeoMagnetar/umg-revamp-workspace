# BATCH-189 - UMG System Overview and Public Canon Reconciliation Review

## Batch Overview
Batch ID: BATCH-189
Source Type: derived summary / internal model versus public canon reconciliation and migration analysis
Working Topic: internal UMG rundown, public spec/compiler review, legacy-versus-current taxonomy shifts, terminology pinning, migration documentation targets
Review Status: REVIEWED
Disposition: ACCEPT_AS_EVIDENCE

## Source Snapshot
The source first generated an internal systems-level rundown of UMG from accumulated conversation context, then shifted into a public-source review of NeoMagCustoms GitHub materials, the linked UMG compiler, archived legacy repository language, and limited X/archive surface.

The strongest recurring themes are:
- internal UMG explanatory structure versus publicly evidenced UMG
- UMG publicly framed as a Cognitive Specification Layer with deterministic compilation into RuntimeSpec and Trace
- explicit contradictions between legacy repo language and current public v0 semantics
- ambiguity around public MOLT role vocabulary and ordering
- split semantics around Trigger / TriggerState, Merge, and stack terminology
- public spec authority over docs and tooling
- need for schemas, conformance reporting, and migration guidance

This source is especially valuable because it does not merely summarize UMG; it distinguishes what is strongly current-public evidence from what is still internal, legacy, provisional, or ecosystem-level language.

## Chat-Level Summary
This batch is strongest as a public-canon reconciliation and migration-target batch.

Its central contribution is the split between:
- internal explanatory UMG
- publicly evidenced UMG

The second strongest contribution is the current strongest public lock:
UMG is framed as a Cognitive Specification Layer that compiles Sleeve JSON into RuntimeSpec and Trace through deterministic structural synthesis.

The third strongest contribution is contradiction surfacing.
The batch explicitly identifies unresolved migration edges around:
- MOLT taxonomy
- Merge as role versus operation
- Trigger block versus TriggerState
- Sleeve / Stack / NeoStack / NeoBlock public pinning
- README/spec/tooling mismatch

## UMG-Relevant Extraction

### Core UMG Semantics
UMG was described internally as a modular cognitive specification and behavior-compilation framework that turns vague intent into governed, typed, reusable, and auditable behavior structures.

The strongest public-facing definition preserved in the source is:
- UMG as a Cognitive Specification Layer framework

The source repeatedly separates intended cognition from execution:
- UMG defines structure
- execution is external
- cognition generation is explicit structural composition plus deterministic resolution

UMG is treated as cross-domain and designed to preserve modular control structure across subject areas.

### MOLT Roles / Taxonomy
The internal rundown preserves recurring MOLT fields:
- Trigger
- Directive
- Instruction
- Subject
- Primary
- Philosophy
- Blueprint

The source then notes that current retrieved public v0 materials require blocks to have a MOLT role, but the retrieved public text did not fully enumerate the full canonical role set or ordering table.

The older archived repo is reported as supplying 9 canonical MOLT block types:
- Primary
- Subject
- Instruction
- Directive
- Philosophy
- Blueprint
- Trigger
- Merge
- Off

The batch treats that older role list as relevant legacy evidence, not automatically as current canon.

### Trigger
The internal rundown treats Trigger as what activates a behavior, stack, or block.
The public-facing layer shifts toward TriggerState semantics:
- synthesis can use explicit state inputs called TriggerState
- governance rules can reference TriggerState
- when TriggerState changes, synthesis reruns to produce a new RuntimeSpec and Trace

The source explicitly flags a split:
- legacy = Trigger as a block type
- current v0 = TriggerState plus synthesis rerun plus governance/OFF framing

TriggerState is treated as present but underspecified in currently retrieved public materials.

### Priority
Priority is described publicly as:
- a deterministic tie-breaker among governance-permitted elements only
- not OFF
- not governance override
- not inferred from content, position, or outcome

The archived repo is reported to include a fixed hierarchy:
- Trigger > Directive > Instruction > Subject > Primary > Merge > Philosophy > Blueprint > Off

The batch explicitly flags tension between:
- legacy fixed cross-role priority hierarchy
- current v0 treatment of priority as explicit declarative conflict resolution

### Merge
The source preserves a direct semantic shift:
- legacy repo treated Merge as a MOLT block type and part of old priority hierarchy
- current v0 materials distinguish merge from bundle and define merge as an explicit composition operation

Current merge in the source is described as:
- declared
- traceable
- creating new cognitive intent
- not happening implicitly by proximity or order

This is one of the clearest migration edges in the batch.

### Bundle
Bundle is explicitly kept separate from merge.
A bundle is described as:
- grouping without semantic fusion
- preserving block identity
- not creating new meaning
- not itself resolving conflicts
- resolved later during synthesis

This batch treats bundle/merge distinction as one of the strongest current public canon signals.

### NeoBlock Composition
The internal rundown defines NeoBlock as a grouped intent or capability cluster inside a NeoStack.
NeoBlocks are described as:
- narrower than NeoStacks
- broader than atomic MOLT blocks
- coherent working units or grouped intent bundles

The public review later notes that NeoBlock terminology appears in broader ecosystem conversation but was not clearly pinned as canonical public v0 spec language in the retrieved materials.

### NeoStack Architecture
The internal rundown defines NeoStack as a major operational domain inside a sleeve.
The scaling logic preserved is:
- NeoStack = domain
- NeoBlock = grouped intent
- MOLT = atomic instruction structure

The public review later flags Stack / NeoStack as not clearly pinned public v0 spec terminology in retrieved sources.
This makes NeoStack a strong internal/ecosystem concept, but not yet clearly stabilized public-spec canon from this batch alone.

### Sleeve Identity / Resleeving
The internal rundown treats Sleeve as a top-level operational package containing:
- purpose
- rules
- domain partitions
- grouped capabilities
- atomic MOLT units
- presentation or behavior constraints

The public-facing layer preserves:
- compiler compiles Sleeve JSON into RuntimeSpec and Trace

The source flags Sleeve as requiring refinement because the retrieved public materials did not fully expose a pinned sleeve schema.

Resleeving was not formalized beyond sleeve-as-container and compiler input.

### Governance / Control
Governance is preserved as one of the strongest canonical layers in the batch.
Internally, governance is described as:
- highest-order rule layer
- what determines what is allowed
- what resolves conflict
- what persists regardless of lower context

Publicly, governance is described as:
- authoritative constraint/policy layer
- enforced before other synthesis mechanisms
- able to set elements OFF
- not overridable by bundles, priority, or merges
- recorded in Trace

OFF is explicitly preserved as:
- exclusion without deletion

### Output Blueprint / Rendering Separation
The source clearly separates structure from output.
Blueprint is treated as a structural template or assembly pattern.
RuntimeSpec is treated as the resolved active structure and contract boundary for external execution systems.
Trace is treated as the forensic record of how synthesis produced that result.
RuntimeSpec excludes governance rationale while Trace carries explanatory/audit content.

### Compiler / Runtime Logic
The source strongly reinforces UMG as compiler-oriented:
- source structure = sleeve / stacks / blocks / MOLT
- intermediate resolution = governance + weights + dominance + activation
- compiled target = RuntimeSpec / prompt assembly / execution bundle
- audit output = Trace

The public review preserves the compiler as:
- separate umg-compiler repo
- canonical reference compiler
- deterministic
- headless
- no model calls
- structural compilation only

Public release details preserved:
- v0.1.0
- January 15, 2026
- commit a8def80

The batch also notes that public materials suggest the spec may be ahead of visible tooling coverage.

### Documentation / Spec Language
The current public canonical source is identified as:
- Universal-Modular-Generation repo /spec/v0

The batch preserves a strong documentation governance signal:
- /spec is authoritative over docs, examples, tooling, and implementations when they disagree

It also flags a direct README/file-tree mismatch:
- README claims broader structure
- visible retrieved file tree appeared narrower

The batch strongly distinguishes:
- current public spec language
- older archived repo language
- internal/ecosystem explanatory terminology

### Safety / Bounded Agency
Governance is treated as the constitutional layer that bounds lower behavior.
Safety is preserved through:
- governance
- OFF semantics
- external execution boundary
- deterministic structural role rather than autonomous runtime agency

The source explicitly keeps UMG in a bounded structural role rather than autonomous execution.

### PRD / Staging / Release
The batch identifies strong next-step refinement targets:
- publish machine-readable schemas
- add normative MOLT roles and ordering document
- clarify whether legacy role hierarchy is deprecated or still normative
- publish compiler conformance matrix
- create legacy v3.0 to spec v0 migration guide

The source treats these as refinement groundwork, not finalized redesign decisions.

## Independent Review
This batch has high Stage 1 value because it is one of the clearest reconciliation artifacts between internal UMG explanatory language and public canon evidence.
Its strongest contribution is not new semantic invention.
It is disciplined separation:
- internal explanatory model
- current public canon signals
- unresolved legacy migration problems

The most important preserved tensions are:
- legacy versus current MOLT taxonomy
- Merge block type versus merge operation
- Trigger block versus TriggerState
- internal NeoStack / NeoBlock / Sleeve usage versus public spec pinning
- README structure claims versus visible public repo tree

Main cautions:
- the internal systems-level rundown was explicitly interpretive
- public confidence was stronger on GitHub/spec/compiler than on X/archive
- several ecosystem terms remain strong conceptually but not fully public-canonical in retrieved v0 materials
- the chat did not finalize redesign decisions, only surfaced refinement targets

## Roadmap Mapping
Primary domain: public canon reconciliation, migration documentation, and spec/compiler refinement targets

Roadmap phases touched:
- PHASE_1_CORE_ALIGNMENT
- PHASE_2_COMPILER_IMPACT
- PHASE_3_DOCUMENTATION_IMPACT
- PHASE_4_SKILL_ALIGNMENT
- PHASE_5_PRD_AND_STAGING
- PHASE_6_GITHUB_EXECUTION
- PHASE_7_RELEASE_READINESS

## Action Outcome
Accepted as evidence.
Frozen as a Stage 1 intake pack.

## Recommended Next Decision
Control-room review should decide how to normalize and promote:
1. current public MOLT role vocabulary and ordering
2. explicit migration path from legacy Merge-as-role to current merge-as-operation
3. Trigger versus TriggerState terminology and activation semantics
4. public pinning or de-emphasis of Sleeve / NeoStack / NeoBlock terminology
5. README/spec/tooling alignment and conformance reporting

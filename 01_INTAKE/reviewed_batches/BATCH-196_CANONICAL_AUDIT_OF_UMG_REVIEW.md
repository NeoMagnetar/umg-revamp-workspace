# BATCH-196 - Canonical Audit of UMG Review

## Batch Overview
Batch ID: BATCH-196
Source Type: derived summary / canon audit, architecture consolidation, and patent-readiness positioning
Working Topic: block grammar plus CSL/control-plane alignment, deterministic compilation, governance-before-execution, artifact model, glossary and schema readiness
Review Status: REVIEWED
Disposition: ACCEPT_AS_EVIDENCE

## Source Snapshot
The source consolidates UMG into a canon-ready multi-layered system and explicitly tries to align:
- block-based UMG grammar
- CSL / control-plane architecture
- compiler artifacts
- governance-first bounded execution
- documentation/schema/patent readiness

The strongest recurring themes are:
- UMG as both a human-facing block grammar and a formal cognitive control architecture
- explicit separation between specification and execution
- deterministic compilation into CIR, RuntimeSpec, and Trace
- governance before execution
- auditability, fail-closed behavior, and bounded execution
- movement toward canonical glossary, schemas, and release artifacts
- unresolved tension around NeoBlock / NeoStack, Merge terminology, and layer boundaries

This source is especially valuable because it does not just refine one term. It assembles the system at architecture level and frames UMG as a standards-ready, patent-ready, canon-ready control model.

## Chat-Level Summary
This batch is strongest as a canon-audit and architecture-consolidation source.

Its central contribution is the integration of two explanatory frames:
- block grammar (Primary / Merge / Blueprint and extended MOLT)
- control-plane / CSL architecture (CSL, Governance, Compiler, CIR, RuntimeSpec, Trace)

Its second strongest contribution is the formal separation:
- specification
- compilation
- execution

Its third strongest contribution is auditability:
- deterministic compilation
- RuntimeSpec as executor contract
- Trace as audit artifact
- fail-closed safety model

## UMG-Relevant Extraction

### Core UMG Semantics
UMG is described as a modular, block-based cognition framework that treats generation as construction rather than prompting.
The source explicitly preserves:
- cognition externalized into artifacts
- pre-runtime cognition
- explicit separation of intent, constraints, and expression
- deterministic compilation pipeline
- specification distinct from execution

Strong system-level framing preserved:
- UMG is both human-facing block grammar and formal cognitive control architecture
- UMG is governance-first cognition with bounded execution

### MOLT Roles / Taxonomy
The source preserves two overlapping layers:
1. Simplified block grammar:
   - Primary
   - Merge
   - Blueprint
2. Extended MOLT taxonomy:
   - trigger
   - directive
   - instruction
   - subject
   - primary
   - philosophy
   - blueprint

Additional block-role terms preserved:
- primary_shell
- merge_contributor
- blueprint_guide

Critical tension preserved:
- alignment between Primary / Merge / Blueprint grammar and the fuller MOLT taxonomy remained incomplete

### Trigger
Triggers are treated as declarative switches, not as something the compiler computes.
The source explicitly preserves:
- Trigger evaluation occurs externally
- compiler consumes TriggerState as input
- TriggerState supports governance conditions and runtime activation
- trigger logic does not construct cognition

### Priority
Priority is preserved as deterministic resolution logic distinct from authority resolution.
The source preserves:
- ranked precedence during compilation/resolution
- deterministic conflict outcomes
- use in governance and block conflict handling

This is one of the stronger signals that the project needs precise language for priority versus authority.

### Merge
The source preserves a major ambiguity:
- Merge Block as must-include content/constraints
- Merge operation as synthesis of blocks into new structure

The audit explicitly flags this dual use as a risk.
It also preserves:
- Merge Block is additive
- conflicts among merges are possible
- merge logic is part of compiler resolution

This batch is valuable because it surfaces the ambiguity directly instead of smoothing over it.

### Bundle
Bundling is preserved as structured grouping of related triggers or directives.
The source states:
- bundling is allowed
- bundles organize rather than redefine semantics
- merge within bundles is rare and advanced
- bundles are for structured composition of control elements

### NeoBlock Composition
NeoBlock is preserved as a derived block created through synthesis or merge operations.
The source treats NeoBlock as:
- a new cognitive/control primitive
- requiring more formal lifecycle definition
- still underdefined enough to need future canon work

### NeoStack Architecture
NeoStack is preserved as a composite block structure representing layered control hierarchy.
The source ties NeoStack to:
- precedence
- authority layering
- orchestration and execution planning

The audit explicitly flags NeoStack authority semantics as still needing clearer formalization.

### Sleeve Identity / Resleeving
Sleeve is preserved as a persistent identity/constraint container and runtime context holder.
The source attributes to Sleeve:
- identity
- long-term constraints
- interaction with governance and scope
- ActiveStack / Sleeve runtime-context linkage

Resleeving is implied but not yet formalized.

### Governance / Control
Governance is one of the strongest preserved layers in the batch.
The source explicitly places Governance above CSL in the control plane and assigns it:
- authority resolution
- priority resolution
- constraints and invariants
- veto / override / constrain behavior
- bounded cognition and behavior before execution

This is a very strong governance-first source.

### Output Blueprint / Rendering Separation
Blueprint Blocks are preserved as defining expression only.
The source states:
- Blueprint must not introduce factual requirements
- cognition is not the same thing as rendering
- rendering occurs after compilation
- Blueprint is a cognitive lens, not a content source

### Compiler / Runtime Logic
The compiler pipeline preserved in the source is:
- Input: Sleeve + TriggerState
- Output: CIR + RuntimeSpec + Trace

Key rules preserved:
- same inputs -> same outputs
- RuntimeSpec governs execution
- executor consumes but does not modify cognition
- Trace records decisions, precedence, and resolution steps
- runtime may include static and dynamic/live compilation modes

This source is especially strong because it preserves all three artifacts together:
- CIR
- RuntimeSpec
- Trace

### Documentation / Spec Language
The source strongly supports canonization through:
- canonical glossary
- YAML/JSON schemas
- normalized terminology
- schema validation
- diff-safe formats
- ASCII key policy
- scope / invariants / non-goals in definitions
- academic terminology mapping where needed

The preserved release path is:
- glossary
- system model
- mechanics
- schemas
- examples
- novelty

### Skill / Agent Workflow
The source frames UMG as:
- cognitive scaffold
- modular workflow layer
- reusable skill-block architecture
- agent interface layer

Preserved workflow:
- assemble blocks
- compile cognition
- execute via agent
- validate and iterate

### Safety / Bounded Agency
Safety is encoded structurally through:
- governance before execution
- RuntimeSpec constraints
- fail-closed semantics
- Decision Trace auditability
- executor cannot exceed RuntimeSpec
- bounded execution rather than reactive safety patches

### PRD / Staging / Release
The source preserves:
- Canon v0 -> v1 process
- release artifacts such as schemas, docs, and example packs
- patent-readiness checklist
- emphasis on auditability, reproducibility, and interoperability

It also explicitly flags open questions that block full finalization.

## Independent Review
This is a major architecture-consolidation batch.
Its strongest contribution is not merely terminology polishing.
It is the assembly of UMG into a coherent control model spanning:
- block grammar
- control plane
- compiler artifacts
- governance-first execution boundaries
- schema and patent readiness

The most important preserved tensions are:
- DCP vs DCEP aliasing / naming cleanup
- MOLT alignment with Primary / Merge / Blueprint
- NeoBlock lifecycle
- NeoStack authority semantics
- Cognitive Envelope vs Sleeve vs RuntimeSpec overlap
- PCL vs MCP boundary clarity
- live compilation trigger rules
- governance override limits
- executor obligations under RuntimeSpec

## Roadmap Mapping
Primary domain: canon audit, architecture consolidation, and artifact model refinement

Roadmap phases touched:
- PHASE_1_CORE_ALIGNMENT
- PHASE_2_COMPILER_IMPACT
- PHASE_3_DOCUMENTATION_IMPACT
- PHASE_4_SKILL_ALIGNMENT
- PHASE_5_PRD_AND_STAGING
- PHASE_7_RELEASE_READINESS

## Action Outcome
Accepted as evidence.
Frozen as a Stage 1 intake pack.

## Recommended Next Decision
Control-room review should decide how to normalize and promote:
1. Primary / Merge / Blueprint grammar relative to the full MOLT taxonomy
2. CIR status and naming relative to RuntimeSpec and Trace
3. governance override semantics and executor obligations
4. NeoBlock / NeoStack lifecycle and authority formalization
5. overlap cleanup among Sleeve, Cognitive Envelope, and RuntimeSpec

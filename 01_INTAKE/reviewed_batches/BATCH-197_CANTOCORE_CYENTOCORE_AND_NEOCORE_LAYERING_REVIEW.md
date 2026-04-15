# BATCH-197 - Cantocore, Cyentocore, and NeoCore Layering Review

## Batch Overview
Batch ID: BATCH-197
Source Type: derived summary / language-layer comparison and toolchain-planning consolidation
Working Topic: Cantocore vs Cyentocore vs NeoCore, layer distinctions, source-to-schema lifecycle, compiler/runtime/tooling roadmap, frontend-first language positioning
Review Status: REVIEWED
Disposition: ACCEPT_AS_EVIDENCE

## Source Snapshot
The source compared Cantocore, Cyentocore, and NeoCore as distinct but cooperating layers within UMG.

The strongest recurring themes are:
- Cantocore as the human-readable intent/philosophy layer
- Cyentocore as the machine-parsable build/execution layer
- NeoCore as the canonical schema/validation contract layer
- a lifecycle of drafting in Cantocore, translating into Cyentocore, and validating/storing through NeoCore
- UMG framed as a possible source language that compiles outward into HTML/CSS/JS and framework targets
- a repo/toolchain roadmap involving parser, validator, transpiler, runtime, CLI, docs, and examples
- an explicit later clarification that the strongest roadmap claims were strategic synthesis rather than a full linked-doc or repo audit

This source is especially valuable because it extends UMG from modular cognition framing into language-system and toolchain framing while also preserving an important evidence-quality caveat.

## Chat-Level Summary
This batch is strongest as a language-layer and toolchain-planning source.

Its central contribution is the three-layer distinction:
- Cantocore = what / why
- Cyentocore = how
- NeoCore = what is structurally allowed and trusted

Its second strongest contribution is the lifecycle:
- draft in Cantocore
- translate into Cyentocore
- validate and store through NeoCore

Its third strongest contribution is the repo and implementation path:
frontend-first language hardening, schema freeze, parser/validator/transpiler/runtime/CLI packages, docs, examples, and later experimental backend generation.

## UMG-Relevant Extraction

### Core UMG Semantics
The source sharpens the distinction among human-facing, machine-facing, and canonical schema layers inside UMG.

Cantocore was described as:
- human-readable intent layer
- philosophy layer
- mission-briefing or song-like language
- conception / ideation surface

Cyentocore was described as:
- machine-parsable build/execution layer
- assembly-instructions or cipher-like syntax
- compilation / build surface

NeoCore was described as:
- canonical schema
- validation contract
- building-code / law layer
- governance / validation surface

The source explicitly preserves the complementary lifecycle:
- Cantocore for ideation
- Cyentocore for machine-facing structured build logic
- NeoCore for validation and trusted storage

### MOLT Roles / Taxonomy
MOLT types appear as explicit typed fields inside machine-readable structures.
The source preserves examples using:
- `molt_type: Subject`
- `molt_type: Blueprint`

This reinforces MOLT as a typed field inside block-level representations.
No role-priority, trigger-order, or hierarchy law is added here beyond typed usage.

### Trigger
Trigger was not materially developed in this chat.
No trigger semantics, trigger state model, or trigger hierarchy work was established here.

### Priority
Priority was not materially developed in this chat.
No explicit priority law or role ordering was established beyond typed examples.

### Merge
Merge was not materially developed in this chat as a formal operation or law.
No merge mechanics, policies, or runtime semantics were established.

### Bundle
Bundle was not materially formalized here.
However, the broader toolchain framing implies that multiple language layers, packages, and example applications may be grouped in a monorepo or release structure.

### NeoBlock Composition
The source includes a concrete example block, `daily_stock_report`, expressed across all three layers.

The block example preserved:
- inputs / requires
- outputs / produces
- snap target
- description / label / category
- tags
- ledger / provenance-like fields in the NeoCore form

The greeting examples also imply that very small self-describing language artifacts can be used as onboarding or documentation blocks.

### NeoStack Architecture
The `daily_stock_report` example snapped into `analytics_stack`.
The source also implies a broader system architecture where stacks matter at both conceptual and compile/runtime levels through snap or snap_config fields.
The repo proposal suggests parser, validator, transpiler, runtime, and CLI packages that would have to preserve stack-relevant information in machine-readable form.

### Governance / Control
NeoCore is the strongest governance signal in the batch.
It is explicitly framed as the place that:
- defines allowed fields
- defines trusted structure
- validates blocks before entry into the system

Governance-adjacent process items proposed:
- semantic versioning
- RFC-based change process
- schema freeze for v1
- naming alignment to reduce public confusion

The source also states that blocks failing schema validation should not enter the system.

### Output Blueprint / Rendering Separation
This is one of the strongest conceptual contributions in the batch.
The source positions UMG as a source language that compiles outward into:
- HTML
- CSS
- JavaScript
- React / Vue / Svelte targets

This preserves a strong distinction between:
- source-layer semantic language
- emitted/rendered implementation assets

The source also frames AI agents as authors of source-language / NeoCore artifacts rather than runtime interpreters.

### Compiler / Runtime Logic
The source proposes or implies the following toolchain pieces:
- parser
- validator
- transpiler
- runtime library
- CLI
- dev server / hot reload
- lazy loading
- state stores
- error maps
- theme scopes
- framework hooks

Proposed CLI commands preserved:
- `umg init`
- `umg dev`
- `umg build`

Backend generation is suggested as later or experimental:
- generate Express / FastAPI endpoints from Instruction blocks
- share contracts between front and back

The source later clarifies that these claims were strategic rather than the result of full repo traversal or low-level runtime audit.

### Documentation / Spec Language
The batch is strong for public-facing layer explanations and onboarding assets.

Analogies preserved:
- Cantocore = mission briefing / song / human-readable logic stanza
- Cyentocore = assembly instructions / cipher / machine-facing syntax
- NeoCore = building code / law / canonical schema

Documentation candidates preserved:
- a shared example rendered in all three layers
- greeting examples for onboarding
- docs-site and examples gallery
- NeoCore JSON Schema v1 freeze
- RFC process
- Docusaurus-style docs and playground

### Skill / Agent Workflow
The source frames AI agents as:
- envoys that write source-language / NeoCore artifacts
- not runtime interpreters

It proposes an AI-native workflow where agents author source blocks and transpilers generate implementation targets.
Detailed skill invocation or tool schemas are not defined here.

### Safety / Bounded Agency
Safety appears through schema validation and trusted structure rather than runtime control logic.
NeoCore is the validation contract layer.
Blocks failing schema validation should not enter the system.
No stronger execution-safety or bounded-agency mechanics are formalized in this chat.

### PRD / Staging / Release
A staged implementation order preserved in the source:
- repository setup
- language hardening
- transpiler expansion
- runtime library
- developer experience
- backend bridge
- beta launch
- stabilization / marketing

Suggested repo structure includes:
- `packages/`
- `examples/`
- `docs/`
- `.github/workflows/`
- `RFCs/`

Release staging suggestions:
- static site example
- SPA/dashboard example
- full-stack example
- beta launch with examples and GitHub Discussions
- backend generation behind experimental flag

## Independent Review
This batch has high Stage 1 value because it turns UMG into a layered language-and-toolchain framing rather than only a modular cognition framework.
Its strongest contribution is the three-layer split among Cantocore, Cyentocore, and NeoCore.
Its second strongest contribution is the lifecycle from ideation to machine-facing form to canonical validation.
Its third strongest contribution is the concrete toolchain/repo planning.

The strongest caution is also explicit and important:
the roadmap and implementation claims were later acknowledged to be strategic synthesis rather than the product of a full linked-document or full repo audit.

Main cautions:
- no trigger, priority, or merge mechanics were materially developed
- public naming architecture remains unresolved
- frontend-first versus full-stack scope remains provisional
- maturity of parser/validator/transpiler/runtime assets was not directly verified here
- backend generation remains directional, not locked

## Roadmap Mapping
Primary domain: language layering, schema validation, compiler/transpiler planning, and frontend-first implementation staging

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
1. public naming strategy for Cantocore / Cyentocore / NeoCore
2. whether NeoCore becomes the primary public-facing schema label or remains one layer among three
3. frontend-first versus wider full-stack language scope
4. how much of the proposed repo/toolchain roadmap is already evidenced versus still aspirational
5. onboarding docs that explain the three layers through one shared example

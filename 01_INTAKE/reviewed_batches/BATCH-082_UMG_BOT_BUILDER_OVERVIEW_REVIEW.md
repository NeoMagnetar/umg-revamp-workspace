# BATCH-082 — UMG Bot Builder Overview — Review

## Batch Overview
- **Batch ID:** BATCH-082
- **Source Type:** derived handoff summary with references to supporting uploaded materials
- **Review Status:** REVIEWED
- **Disposition:** ACCEPT_AS_EVIDENCE
- **Primary Domain:** builder_semantics
- **Evidence Strength:** medium-high
- **Why it matters:** this batch clarifies a major semantic distinction between UMG as architecture and MOLT as user-facing grammar, then ties that distinction to concrete builder behavior, hierarchy, merge semantics, and product staging.

## Source Snapshot
- The source summarizes a chat about translating UMG into a more explicit compositional language and builder workflow.
- It presents MOLT as a clarified semantic grammar on top of UMG rather than a replacement for UMG.
- It introduces practical UI concerns:
  - four visible role types
  - example presets
  - snapping
  - stacking
  - merge-any-block behavior
  - skeleton mode
  - future searchable block database
- It also notes tension with earlier uploaded documents that still emphasize Blueprint / Merge / Instruction terminology.

## Chat-Level Summary
This batch is one of the clearer bridge artifacts between high-level UMG theory and builder-facing implementation. Its strongest contribution is semantic reframing: **UMG = architecture / scaffolding**, **MOLT = grammar / operating language of thought**. From that clarification, the batch develops concrete implications for the builder surface, including role taxonomy, hierarchy rules, merge behavior, scoped branch logic, visual semantics, and staged product requirements. The batch remains evidence rather than canon because naming, color mapping, priority treatment, and merge behavior are still partially in motion.

## UMG-Relevant Extraction
### Core Semantics
- UMG is treated as a modular cognition architecture, not a monolithic prompt.
- Outputs are constructed from reusable blocks that can be stacked, snapped, merged, and reused.
- The same system is expected to support bots, stories, plans, poems, and structured outputs.
- UMG is presented as a universal compositional engine.

### MOLT Grammar Layer
- MOLT is clarified as the user-facing compositional grammar layered on top of UMG.
- The working role set converges on:
  - Template / Primary
  - Subject
  - Philosophy
  - Instruction
- Plain-language meaning of the role set:
  - what to do
  - what it is about
  - how to think
  - how to behave

### Merge / Hierarchy
- Merge is broadened beyond support-info-only semantics.
- Any block types may become merge candidates.
- Philosophies and instructions may apply globally, partially, or to specific branches.
- Merged blocks should visibly indicate composition and summarize contents.
- Hierarchy should support both:
  - inherited top-down structure
  - equal-authority peer structures
  - branch-scoped logic

### Builder / Product Surface
- Concrete features surfaced:
  - four visible block types
  - five example presets per type
  - custom user content
  - snapping and stacking
  - merged-core generation
  - lower-hierarchy attachments
  - skeleton mode
  - future searchable database-backed block library
- The builder is broadened from a narrow bot composer into a more general modular composition system.

## Independent Review
This is a strong **builder-facing semantics batch**. It helps solve a recurring usability problem: earlier UMG language is rich but can be opaque to users, while this batch tries to expose a clearer operational grammar without discarding the underlying architecture. That makes it valuable for:
- documentation harmonization
- builder PRD scoping
- role legend design
- object-model refinement
- future compiler alignment

Its main weakness is instability at the naming and boundary level:
- Template vs Primary vs Blueprint vs Goal are not fully settled
- instruction merge behavior remains intentionally flexible
- hierarchy vs peer authority remains unresolved
- earlier numeric priority/token-weight semantics are not fully reconciled with the newer builder-facing framing

## Roadmap Mapping
- **PHASE_1_CORE_ALIGNMENT:** UMG vs MOLT distinction, role taxonomy stabilization, merge semantics
- **PHASE_2_COMPILER_IMPACT:** snapped hierarchy, merged core nodes, block typing, runtime graph shape
- **PHASE_3_DOCUMENTATION_IMPACT:** glossary, framework cards, builder legends, whitepaper harmonization
- **PHASE_4_SKILL_ALIGNMENT:** agent / skill composition workflow, reusable block presets, future block database
- **PHASE_5_PRD_AND_STAGING:** MVP builder scope, staged rollout, skeleton mode, searchable presets

## Action Outcome
- Accepted as evidence.
- Default four-file pack created.
- Optional extracts created only for:
  - compiler/runtime builder semantics
  - blocks/MOLT taxonomy
  - higher-order hierarchy / skeleton structure
  - contradiction / ambiguity tracking

## Recommended Next Decision
Decide whether the project wants to standardize the user-facing grammar as:
- Template / Subject / Philosophy / Instruction
or
- Primary / Subject / Philosophy / Instruction
while explicitly documenting how this maps back to existing Blueprint / Merge / Instruction terminology.

# BATCH-169 — UMG Block Metadata Builder Review

## Source Snapshot
This batch is a builder-focused intake source about turning UMG from a loose conceptual/repo structure into an explicit, self-describing block system with canonical JSON blocks, clearer schema naming, sleeve-loading consistency, and a staged builder app path. It also includes repo cleanup and migration notes for the current UMG-BUILDER codebase. Source remains evidence only and is not canon. fileciteturn19file0

## Chat-Level Summary
The strongest signal in this source is the push toward **fully encoded UMG blocks** rather than abstract descriptions. Blocks are expected to carry identity, MOLT role, snap behavior, merge behavior, runtime flags, provenance, optional code modules, and display metadata directly inside each JSON object. The source also tightens the builder product concept: left-side visual composition, right-side live JSON, drag/drop stacking, snap behavior, manual/automatic merge decisions, optional Poe assistance, and import/export-first rollout. In parallel, it identifies repo cleanup work: canonical `blocks/` root, sleeve loader unification, registry repair, schema-key normalization, and removal of stale or duplicate paths. fileciteturn19file0

## UMG-Relevant Extraction
- Blocks are the atomic unit of builder logic and must be self-describing.
- Canonical core MOLT types were explicitly enumerated as JSON blueprints: Primary, Subject, Instruction, Directive, Philosophy, Blueprint, Trigger, Deployment, Off; Merge was later added as a candidate/operator-style canonical block. fileciteturn19file0
- Snap, stack, and merge are treated as first-class encoded behavior, not external interpretation.
- Builder runtime is expected to expose block structure visibly through a side JSON panel and drag/drop graph/canvas interactions.
- Sleeves are concrete runtime state objects loaded from `sleeves/*.json`, with active sleeve content copied into `memory/active_state.json`.
- Repo/runtime tasks include: canonical folder cleanup, sleeve loader consolidation, command registry repair, schema field rename migration, and future validation/merge engine work. fileciteturn19file0

## Independent Review
This is a high-value Stage 1 source because it moves UMG from “logic language” rhetoric into implementation obligations. Its strongest contribution is not a new philosophical claim; it is the demand that blocks encode their own compositional and runtime semantics. That matters for all later compiler, builder, documentation, and skill work. At the same time, the source preserves unresolved tension that must not be flattened at intake:
- `cantocore` vs `canto_overlay`
- `merge_logic` vs `merge_behavior`
- whether Merge is fully canonical or still a candidate/operator block
- role/color inconsistencies around Deployment
- partial repo/path ambiguity during cleanup work. fileciteturn19file0

## Roadmap Mapping
- **Phase 1 — Core Alignment:** tighten canonical block ontology, role names, and encoded snap/merge semantics.
- **Phase 2 — Compiler Impact:** normalize schema keys, loader behavior, merge engine expectations, and sleeve activation behavior.
- **Phase 3 — Documentation Impact:** stabilize the schema guide, color grammar, directory conventions, and copyable examples.
- **Phase 4 — Skill Alignment:** expose stable registry repair, sleeve loading, and builder-assist command paths.
- **Phase 5 — PRD/Staging:** Bolt.new builder MVP, import/export-first rollout, optional Poe assistance, staged 800-block scaling. fileciteturn19file0

## Action Outcome
**Disposition:** `ACCEPT_AS_EVIDENCE`

Rationale: this batch is coherent, implementation-facing, and structurally useful, but it still contains active schema inconsistencies and at least one unresolved ontology question around Merge. It should therefore remain in intake as reviewed evidence rather than be promoted directly into canon.

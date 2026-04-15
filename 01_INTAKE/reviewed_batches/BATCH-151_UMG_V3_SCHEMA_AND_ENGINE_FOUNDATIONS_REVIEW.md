# BATCH-151 — UMG v3 Schema and Engine Foundations Review

## Batch Overview
Batch ID: BATCH-151  
Source Type: derived summary / schema, taxonomy, engine behavior, and repo-structure consolidation  
Working Topic: UMG v3.0 block schema, MOLT taxonomy, Snap/Merge/Stack mechanics, mergeable Primary tension, Citadel planning stack, repo/tooling structure  
Review Status: REVIEWED  
Disposition: ACCEPT_AS_EVIDENCE

## Source Snapshot
The source refines the UMG block system and schema at a canon-facing level. It covers MOLT taxonomy and role boundaries, example block implementations, Snap/Merge/Stack mechanics, Citadel planning-stack usage, scaffold/tooling ideas, documentation refinement, and repo layout for NeoUMG / UMG Citadel.

## Chat-Level Summary
This batch is strongest as a canon-facing foundation pass. Its main contribution is the v3.0 working definition of MOLT roles plus the practical JSON block schema that carries them. It also links ontology to mechanics: one-role-per-block discipline, core engine operations, blueprint/render separation, runtime flags, merge fields, and a concrete repo/tooling path.

## UMG-Relevant Extraction
The source explicitly defines:
- MOLT = Modular Operating Language of Thought
- UMG = Cognitive Operating System
- blocks as atomic units of thought

Canonical v3.0 MOLT types surfaced:
- Primary
- Subject
- Instruction
- Directive
- Philosophy
- Blueprint
- Trigger
- Merge
- Off

Role separation is clarified as:
- Instruction = logic / constraints
- Philosophy = ethics / tone
- Blueprint = formatting / layout
- Directive = strategy / mutation layer

Trigger blocks do not inject prompt text. They are used for activation, flow control, and UI behavior, and execute independently rather than being merged.

Priority appears through runtime flags such as `render_injection_priority` and `is_primary_directive`, plus a merge priority hierarchy:
Trigger > Directive > Instruction > Subject > Primary > Merge > Philosophy > Blueprint > Off

Merge is same-type combination when compatible. Strategies include additive, override, and layered. Merge-related fields include:
- `merge_as`
- `merge_strategy`
- `merge_origin`

The source also raises a major tension: Primary blocks may become mergeable through `parent_context_mode: "mergeable"`.

Bundle logic appears through vaults, sleeves, project templates, sleeve presets, and default merge stacks.

NeoBlock composition is concrete through repeated schema fields:
- `block_id`
- `label`
- `description`
- `editable_fields`
- `runtime_behavior_flags`
- `snap_config`
- `canto_overlay`
- `ledger`
- `export_config`
- `code_modules`

Blocks can also expose tools through `function_spec`.

NeoStack architecture is explicitly layered:
Primary → Subject → Instruction → Blueprint → Philosophy

Governance/control is spread across runtime flags, ledger enforcement, and MCP-like control-plane ideas. Blueprint/render separation is explicit: Blueprint handles formatting only, Instruction must not handle formatting, Philosophy must not handle structure. Export formats mentioned include json, md, tsx.

Compiler/runtime logic is proto-concrete through `mergeEngine.js`, Snap/Merge/Stack engine operations, `code_modules`, and `function_spec`.

## Independent Review
This is one of the clearest schema-and-engine foundation sources in intake. Its strongest contribution is the practical union of ontology and mechanics. The mergeable Primary question is especially important because it moves the project from strict hierarchy toward flexible higher-order composition without resolving the consequences.

## Roadmap Mapping
Primary domain: MOLT canon, block schema, and core engine mechanics

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
Optional compiler extract, blocks/MOLT extract, canon candidates, and contradiction flags are justified because the source contains schema law, engine behavior, canon-facing vocabulary, and unresolved structural tensions.

## Recommended Next Decision
Control-room review should decide how to normalize and promote:
1. v3.0 MOLT taxonomy as current working canon
2. final rule for mergeable Primary versus single Primary
3. Directive versus Instruction role boundary
4. canonical Snap / Merge / Stack engine semantics
5. stable schema field set across evolving block examples

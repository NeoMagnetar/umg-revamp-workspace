# BATCH-182 - UMG Builder Block Repair and Runtime Patterns Review

## Batch Overview
Batch ID: BATCH-182
Source Type: derived summary / Builder implementation repair and runtime pattern consolidation
Working Topic: static block architecture, manifest-driven stack loading, MOLT-organized block packs, Builder-vs-framework boundary, Bolt-ready runtime repair
Review Status: REVIEWED
Disposition: ACCEPT_AS_EVIDENCE

## Source Snapshot
The source focused on operationalizing UMG Builder as a Bolt-ready web app that expresses UMG through static `.block.json` files organized by MOLT type.

The strongest recurring themes are:
- Builder as a concrete implementation surface over the broader UMG framework
- static file-based runtime logic with no database requirement
- manifests as stack auto-population sources
- snap, stack, merge, trigger, deployment, and manifest logic as Builder runtime surfaces
- missing metadata repair and underpopulated MOLT pack generation
- correcting folder structure and Git placement
- preparing repo documentation and deployment readiness for Bolt

This source is especially valuable because it shows UMG not as abstract canon only, but as a practical Builder runtime made from static blocks, manifests, matrices, and scripts.

## Chat-Level Summary
This batch is strongest as a Builder implementation and runtime-pattern source.

Its central contribution is the implementation boundary:
- UMG is the framework
- UMG Builder is one JSON-based tool and interface built on top of it

The second strongest contribution is the static runtime model.
The Builder is expected to load modular block files, apply manifest-driven plan selection, use stack priority and snap compatibility, respect merge and trigger logic, and remain file-based rather than database-backed.

The third strongest contribution is release and repair realism.
The chat repeatedly dealt with missing metadata, missing blocks, wrong folder placement, manifest relocation, and repo-state ambiguity between local, GitHub, and generated assets.

## UMG-Relevant Extraction

### Core UMG Semantics
- UMG was treated as a modular cognition framework, not merely a UI app.
- The Builder was framed as one implementation surface that loads `.block.json` files in UMG format.
- The Builder supports drag, drop, stack, snap, merge, edit, and export behavior.
- Static JSON files, not a database, were treated as the core logic substrate.
- Blocks were treated as composable units of thought and logic.

### MOLT Roles / Taxonomy
The active Builder-facing MOLT taxonomy in the source consisted of:
- Primary
- Subject
- Instruction
- Philosophy
- Blueprint
- Directive
- Trigger
- Deployment
- Off

A provisional Meta category also appeared later for runtime or agent overlay ideas such as:
- meta_agent_context
- meta_plan_role
- meta_ai_overlay
- meta_user_persona_ref
- meta_plan_template_type

Builder-facing role meanings were operationalized as:
- Primary = anchor or main plan intent
- Subject = domain or topic focus
- Instruction = rule or actionable execution layer
- Philosophy = tone, worldview, or alignment overlay
- Blueprint = layout, render, or view logic
- Directive = strategy overlay that can affect other blocks
- Trigger = event-based activation logic
- Deployment = export or runtime target logic
- Off = retained but disabled logic

### Trigger
Trigger logic was elevated as necessary for runtime-reactive behavior.
The source preserves Builder trigger examples such as:
- trigger_on_stack_load
- trigger_on_plan_select
- trigger_on_user_role_change
- trigger_on_block_edit
- trigger_on_export
- trigger_on_save
- trigger_on_manifest_loaded
- trigger_on_template_apply
- trigger_on_stack_merge
- trigger_on_trigger_fire

Additional system-level triggers also appeared:
- on_token_limit
- on_merge_conflict
- on_ai_suggestion
- on_system_refresh
- on_snapshot_restore

Trigger blocks were modeled as:
- `molt_type: "Trigger"`
- snapped to Primary
- high stack priority relative to runtime activation
- event-based rather than content-based

### Priority
Vertical stack ordering was explicit.
A core stack priority mapping used in the source:
- Primary: 0
- Subject: 1
- Instruction: 2
- Directive: 3
- Philosophy: 4
- Blueprint: 5
- Trigger: 6 or runtime-priority layer
- Deployment: 7 or later
- Off: 99

The source also states that array order in manifests represents stacking order within each MOLT group.

### Merge
Merge logic was treated as one of the missing core pieces needed to make Builder blocks interoperate.
The chat established both:
- a global `mergeMatrix.json`
- per-block `merge_behavior`

Merge behavior fields included:
- `merge_as`
- `merge_strategy`
- `merge_origin`

Directive blocks were especially treated as overlay logic that can modify Instruction or Philosophy behavior.
Manifest and runtime logic were both expected to respect merge rules.

### Bundle
Builder runtime used bundle-like drop-ins such as:
- philosophy block packs
- directive block packs
- trigger pack
- off/deployment pack
- final logic extension pack
- manifest stub block pack

The app itself was described as a bundle of:
- `data/blocks/`
- scripts
- manifest files
- matrix files
- README and docs

### NeoBlock Composition
Blocks were treated as full modular objects with recurring fields such as:
- block_id
- label
- description
- category
- molt_type
- tags
- cantocore
- snap_config
- merge_behavior
- stack_priority
- canto_overlay
- display
- editable_fields
- ledger

Blocks were expected to carry enough self-description to behave independently, not rely only on global matrices.

### NeoStack Architecture
The stack was consistently represented as:
- Primary
- Subject
- Instruction
- Directive
- Philosophy
- Blueprint

The stack could be auto-built from:
- manifests
- cantocore tags
- plan-type selection

The Builder app was expected to:
- auto-populate a stack from manifests and templates
- order blocks by stack priority
- apply snap and merge behavior live
- save, export, preview, clone, rebuild, and validate stacks

### Governance / Control
The source did not introduce new framework-wide governance canon, but it did add Builder-facing control concepts through:
- Directive overlays
- Off toggles
- readonly and preview modes
- minimal mode
- fast draft mode
- snap override concepts

Repo and filesystem correctness became part of Builder trust and control because the app needed to reflect actual local repo state.

### Output Blueprint / Rendering Separation
The source strongly separates:
- UMG framework semantics
- Builder rendering implementation

Blueprint blocks were treated as rendering or UI overlays rather than core semantic logic.
Philosophy remained tone or alignment.
Instruction remained behavior and execution logic.

### Compiler / Runtime Logic
The source produced concrete runtime logic assets:
- `snapMatrix.json`
- `mergeMatrix.json`
- `update_stack_logic.py`
- `autopopulate_stack.py`
- `validate_manifest_refs.py`

These were used for:
- injecting stack priority and snap config
- loading and sorting blocks by tags or cantocore
- building stacks
- validating manifest references against actual block files

The runtime model was explicitly file-based:
- no backend required
- no database required
- static JSON as the logic substrate

### Documentation / Spec Language
Documentation surfaces discussed in the source included:
- `README.md`
- `UMG Builder Web - Template Manifest Format`
- `UMG Block Schema Reference`

The manifest documentation was refined to explicitly separate:
- UMG framework
- UMG Builder implementation

Manifest spec details preserved in the source:
- location: `/apps/umg-builder-web/manifests/`
- flat JSON keyed by MOLT type
- values are arrays of block_id values
- array order equals stack order
- one Primary recommended
- validation via `validate_manifest_refs.py`

### Skill / Agent Workflow
The repo was framed as eventually supporting agent-usable UMG logic.
Meta/runtime blocks introduced agent-like concepts such as:
- agent context
- plan role
- AI overlay
- user persona reference
- template type

The Builder was explicitly treated as a stepping stone toward future agent overlays while still remaining non-AI in its current app form.

### Safety / Bounded Agency
The source preserves bounded operational controls such as:
- Off blocks
- readonly preview modes
- no-edit mode
- validation suspension toggles
- preview-only logic

A recurring trust rule is preserved:
the system must not claim a file or change exists unless it actually exists in the local repo.

### PRD / Staging / Release
The Builder was treated as a Bolt hackathon deliverable with release pressure.
Working release structure included:
- `data/blocks/`
- `scripts/`
- `apps/umg-builder-web/manifests/`
- root matrix files
- README and docs

The user explicitly asked what still needed cleaning before bolting it on, which led to:
- manifest placement
- folder flattening
- nested extraction cleanup
- final repo audit

## Independent Review
This batch has high Stage 1 value because it turns UMG into a concrete Builder runtime pattern rather than only conceptual canon.
Its strongest contribution is the framework-versus-builder boundary.
Its second strongest contribution is the static-file runtime model.
Its third strongest contribution is the operational repair and staging realism around blocks, manifests, matrices, and repo drift.

Main cautions:
- Meta is useful in this chat but may remain a Builder/runtime extension rather than long-term canon
- some generated blocks or manifest references were provisional or stub-based
- final counts and final cleaned folder state were not fully audited in one definitive pass
- the source strongly supports Builder runtime logic but does not finalize UMG-wide canon beyond this implementation context

## Roadmap Mapping
Primary domain: Builder runtime implementation, static block architecture, and manifest-driven stack behavior

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
1. Builder-vs-framework boundary language
2. Builder-specific manifest and matrix runtime docs
3. status of Meta as Builder extension versus canon role
4. static-file runtime assumptions as PRD language
5. repo reconciliation rules for local, GitHub, and generated assets

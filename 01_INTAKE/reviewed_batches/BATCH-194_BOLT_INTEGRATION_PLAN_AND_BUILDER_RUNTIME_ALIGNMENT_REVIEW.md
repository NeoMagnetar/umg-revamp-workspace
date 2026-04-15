# BATCH-194 - Bolt Integration Plan and Builder Runtime Alignment Review

## Batch Overview
Batch ID: BATCH-194
Source Type: derived summary / builder-runtime stabilization, Bolt integration, and app-structure alignment consolidation
Working Topic: canonical builder app path, block JSON loading, route/file-tree cleanup, snap/stack/merge runtime behavior, builder UX stabilization, staged Bolt/Git workflow
Review Status: REVIEWED
Disposition: ACCEPT_AS_EVIDENCE

## Source Snapshot
The source focused on getting a UMG Builder web app running inside Bolt, fixing routing and file-structure confusion, and restoring the intended builder UI instead of a separate landing page.

The strongest recurring themes are:
- UMG Builder as a visual modular system built around MOLT blocks
- builder runtime issues such as missing block files, duplicate app structures, bad preview behavior, and port conflicts
- block snapping, stacking, merging, zooming, side-panel behavior, templates, and domain starter packs
- manifest- and JSON-driven block definitions
- clear separation between landing-page rendering and builder/canvas rendering
- Git/Bolt/Windsurf workflow boundaries
- need for one canonical app path and one canonical source tree

This source is especially valuable because it grounds UMG in a live builder/runtime product and exposes concrete integration, loading, and file-structure constraints.

## Chat-Level Summary
This batch is strongest as a builder-runtime alignment and integration batch.

Its central contribution is the insistence that there must be one canonical builder app path and one canonical file tree. The repeated confusion between root-level app content and `apps/umg-builder-web` is treated as a serious blocker.

Its second strongest contribution is real runtime logic for the block engine:
- load block JSONs
- classify by `molt_type`
- validate snap compatibility
- merge blocks deterministically
- apply manifests and stacks against actual files

Its third strongest contribution is product staging realism.
The source makes clear that Bolt is useful for preview, but trustworthy coding and syncing should probably move through Git/editor-native workflows rather than unreliable browser-agent automation.

## UMG-Relevant Extraction

### Core UMG Semantics
UMG is treated here as a modular AI builder built around MOLT Blocks.
Repeated working language preserved in the source:
- Modular AI builder powered by MOLT Blocks. Snap. Stack. Compose.

The builder is framed as a visual modular composition system where blocks can be:
- loaded
- arranged
- edited
- merged
- exported
- used to generate structured outputs such as plans, websites, and chatbots

The canvas is treated as a graph/composition runtime in which blocks represent modular thought or function units.

### MOLT Roles / Taxonomy
The chat repeatedly used a nine-lane MOLT order:
- Trigger
- Directive
- Instruction
- Subject
- Primary
- Blueprint
- Philosophy
- Deployment
- Off

MOLT types act as both:
- taxonomy
- runtime priority/signature for loading and handling blocks

The source expects sidebar filtering by `molt_type`, with category lists generated from JSON block definitions and unique role values.

### Trigger
Trigger is explicitly part of the MOLT ordering and loader logic.
Trigger blocks are expected to exist as JSON files under paths like:
- `/data/blocks/Trigger/...`

Example trigger-oriented stock-market blocks mentioned:
- Price Spike
- Gap Open
- Whale Buy

A specific missing Trigger block ID is preserved in the source:
- `bp__Trigger_conversation_start`

Trigger also functions as a runtime event layer for auto-fired behavior such as alerts and webhooks.

### Priority
Priority logic is explicitly part of the proposed block engine.
The source treats MOLT sequence as a candidate priority order.
One implementation sketch uses numeric priority where earlier MOLT positions determine snap/merge precedence.
The UI was expected to show priority indicators on blocks, such as:
- tiny colored dot 1-5
- visual priority tags

Priority also contributes to snap behavior so blocks connect logically and preserve hierarchy.

### Merge
Merge is treated as a core engine behavior paired with snap.
A candidate pattern preserved in the source:
- `mergeBlocks(a,b)`

The source frames merge as copying or overlaying block properties while preserving identity fields.
Merge is expected to be:
- schema-driven
- deterministic
- preceded by can-snap validation
- influenced by block priority and type compatibility

Builder copy also repeatedly promises:
- snap and merge
- stack and merge
- seamless block merging

### Bundle
Bundle logic appears through stack/preset/export behavior rather than a formal doctrine.
The source implies:
- stacks can be saved, imported, exported
- selected blocks or packs can form domain starter packs
- chatbot and stock-market packs can represent reusable grouped block collections

Bundle here is primarily a pack/preset/export surface.

### NeoBlock Composition
Blocks are assumed to be JSON-defined modular units with fields such as:
- `block_id` or `id`
- `title` or `label`
- `description`
- `molt_type`
- `priority`
- `props`
- `inputs`
- `outputs`
- `icon`
- `tags`

The source also preserves a "New Block" flow using a form that appends or writes a new block definition into the library.
The builder is expected to be populated by real authoritative block JSON rather than placeholders.

### NeoStack Architecture
The builder explicitly supports stacks of blocks on a canvas.
The source preserves:
- "0 blocks on canvas"
- presets and stacks such as business plan, web app, chatbot, stock-market system
- manifest examples mapping MOLT lanes to block IDs
- savable, exportable, and reusable JSON packs

Plan-specific stacks may be selected through plan pickers or category tabs.

### Governance / Control
This batch does not add new constitutional doctrine, but it strongly reinforces builder control surfaces:
- one canonical app path
- one canonical file tree
- one correct default route
- one authoritative block source
- reduced opaque automation

Bolt auto-edits and browser-agent behavior are treated as unreliable.
The source therefore favors simple, auditable steps over opaque browser control.

### Output Blueprint / Rendering Separation
This is one of the strongest contributions in the batch.
The chat repeatedly separates:
- marketing or landing rendering
- builder/canvas rendering

A direct distinction emerged between:
- root-level `index.html` and root `src` legacy or landing content
- `apps/umg-builder-web/src` as the actual builder application

The source also emphasizes that blocks are defined by JSON/schema while components such as Canvas, BlockLibrary, and JsonEditor are only render/edit layers.

### Compiler / Runtime Logic
Runtime issues are central to this batch:
- wrong app served
- wrong port
- wrong source tree edited
- missing block JSONs
- invalid drag/drop JSON parsing
- dev server conflicts

Candidate block-engine logic preserved:
- `load(id)`
- `canSnap(target, incoming)`
- `mergeBlocks(a,b)`
- hot-reload for block JSON
- loader reading `public/data/blocks/**/*.json`

Explicit missing-block lookup paths preserved:
- `/data/<id>.block.json`
- `/data/blocks/<MOLT>/<id>.block.json`

The batch also preserves a drag/drop runtime failure:
- Unexpected end of JSON input

This is strong implementation-facing runtime evidence.

### Documentation / Spec Language
The source preserves multiple plain-English candidate product phrases:
- Modular AI builder powered by MOLT Blocks. Snap. Stack. Compose.
- Your MOLT canvas awaits
- 0 blocks on canvas
- Block Library
- Block Inspector

It also produces draft implementation-spec language such as:
- scaffold folders
- load block JSONs
- classify by `molt_type`
- create new block form
- add stock pack
- fix zoom and panning

### Skill / Agent Workflow
The source repeatedly explores AI-assisted workflows using:
- Bolt
- Windsurf
- VS Code
- GitHub
- Operator-like browser agents
- editor-native assistants

Browser-agent control is treated as unstable.
Git-centric or editor-native workflows are framed as more reliable.
A candidate working pattern preserved:
- keep code in GitHub
- let AI edit via repo/Git rather than browser clicks
- use Bolt for live preview and UI checks

### Safety / Bounded Agency
Safety here is mainly operational:
- avoid wrong-source editing
- avoid duplicate trees
- avoid opaque auto-actions
- keep runtime aligned with actual file paths
- prefer auditable steps

This is a bounded builder/runtime-control batch rather than a policy-philosophy batch.

### PRD / Staging / Release
The source explicitly references missed hackathon timing and continued value in finishing the builder properly afterward.
A staged rollout preserved in the source:
- stabilize file structure and runtime
- get block library working
- fix zoom and panel behavior
- add stock-market pack and later NLP/ghost features

A strong migration note preserved:
- remove duplicate root `src`
- keep `apps/umg-builder-web/src` as canonical builder app
- route or rename legacy landing page as needed

## Independent Review
This batch has high Stage 1 value because it grounds UMG in a real builder/runtime integration problem rather than abstract semantics alone.

Its strongest contribution is the canonical-path doctrine:
one builder app, one source tree, one runtime reality.

Its second strongest contribution is concrete load/snap/merge/runtime behavior.
Its third strongest contribution is the separation between schema-defined blocks and the builder surface that renders and edits them.

Main cautions:
- some earlier implementation advice in the chat was wrong because file paths were misunderstood
- the schema summary was not re-verified line by line against the canonical file during that conversation
- routing decisions remained unresolved
- Git/Bolt/Windsurf workflow boundaries were not fully settled
- domain packs and templates remain candidate content rather than canon

## Roadmap Mapping
Primary domain: builder-runtime stabilization, canonical app-path alignment, and JSON block loading

Roadmap phases touched:
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
1. canonical builder app path and source-tree doctrine
2. required block JSON naming and path conventions
3. standard `load / canSnap / mergeBlocks` runtime contract
4. route split between landing page and builder
5. preferred AI-assisted workflow across Bolt, Git, and editor-native tools

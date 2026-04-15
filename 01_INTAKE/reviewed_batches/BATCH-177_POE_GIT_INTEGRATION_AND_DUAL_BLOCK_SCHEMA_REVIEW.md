# BATCH-177 — Poe Git Integration and Dual Block Schema Review

## Batch Overview
Batch ID: BATCH-177  
Source Type: derived summary / repo-operable agent workflow and schema design consolidation  
Working Topic: Poe repo integration, Cantocore priority, NeoCore schema, lightweight block mode, codespace terminal actions, schema-aware runtime behavior  
Review Status: REVIEWED  
Disposition: ACCEPT_AS_EVIDENCE

## Source Snapshot
The source captures a practical implementation-oriented session focused on getting Poe UMG operational in a Git-backed repo or codespace environment.
The strongest themes are:
- Cantocore as the immediate priority
- distinction between Cantocore and Cyentocore
- need for a Cantocore master key
- need for a second master key for block data and metadata
- a rich NeoCore modular block schema
- tension between metadata-heavy canonical blocks and lightweight everyday blocks
- natural-language repo operations through Poe in terminal/codespace
- schema-aware runtime validation and commit workflows

This source is especially valuable because it moves from abstract UMG discussion into concrete storage, schema location, runtime agent behavior, file operations, and repo action patterns.

## Chat-Level Summary
This batch is strongest as a practical execution bridge between UMG concepts and real repo-operable agent behavior.
Its central contribution is not a new canon ontology by itself, but a live design problem:
how should Poe understand and act on structured UMG logic inside a Git/codespace workflow?

The strongest reusable signal is the emergence of a **dual block philosophy**:
- rich canonical or production-grade blocks with full metadata and recursive structure
- lighter everyday blocks that are faster to author and easier to use in normal work

The second strongest contribution is schema placement and runtime behavior.
The source identifies a concrete schema file location, validation approach, and runtime loop for an agent that can interpret natural language, ask clarifying questions, manipulate repo files, and commit work.

The third strongest contribution is Cantocore priority.
Cantocore is treated as the human-visible logic layer Poe must understand first, while Cyentocore remains more internal and less settled.

## UMG-Relevant Extraction
Cantocore is described as condensed language logic for visible human-to-agent communication.
Cyentocore is remembered as a more compressed internal system language used when no user-facing output is needed.
Cantocore is treated as the immediate priority and is said to require a **master key**.

A second master key is proposed for block data and metadata.
This indicates centralized definitional control over:
- what blocks are
- how they store structure
- how much metadata they require
- how agents should interpret them

The NeoCore Modular Block Schema is a major preserved signal.
Required fields in the supplied schema are:
- `block_id`
- `label`
- `category`
- `molt_type`
- `body`
- `ledger`

The schema also supports:
- recursive body composition
- embedded block-like objects
- reference objects using `ref`
- `code_modules`
- `dependencies`
- `editable_fields`
- `display`
- `tags`
- `snap_config`
- `stack`

`molt_type` enum values in the supplied schema include:
- Primary
- Subject
- Instruction
- Directive
- Philosophy
- Blueprint
- Merge
- Trigger
- CodeBlock
- Off

This batch therefore preserves evidence of a richer schema layer that still contains older or broader taxonomy assumptions compared with some later compiler-safe canon.

Trigger is explicitly first-class in the richer schema through a `trigger` object with:
- `event`
- `target`
- `condition`
- `actions`

Priority appears in two places:
- `merge_behavior.priority`
- `snap_config.priority`

Merge is represented structurally through:
- `rules.auto_merge`
- `rules.mutation_rule`
- `rules.merge_strategy`
- `merge_behavior.strategy`
- `merge_behavior.priority`
- `merge_behavior.overrides`
- `merge_behavior.conflict_resolution`

This source does not finalize merge canon, but it clearly preserves a richer metadata-heavy merge surface.

NeoBlock composition is concrete.
Blocks can be recursive, code-bearing, dependency-aware, and metadata-rich.
At the same time, the source introduces a competing practical philosophy:
everyday blocks may be much lighter, keeping only fields such as:
- `block_id`
- `label`
- `category`
- `molt_type`
- simple `body`

This creates a clear design tension between:
- maximum structure for validation/provenance
- minimum structure for daily usability

NeoStack architecture is present structurally through:
- `stack`
- `snap_config`
- grouping identifiers
- hierarchical or grouping semantics
but not fully formalized into a broader runtime theory here.

Sleeves are acknowledged as needing updates for Poe.
The source explicitly notes that Poe’s blocks and sleeves need alignment with Cantocore and the evolving block approach.
However, sleeve schema and migration logic remain unspecified.

Governance/control is operational rather than philosophical in this batch.
The user wants:
- full practical autonomy
- but clarification prompts when parameters are missing
This yields a bounded control pattern based on:
- clarification fallback
- schema validation
- repo file structure discipline
- commit workflow

Compiler/runtime logic is particularly important here.
The source proposes:
- storing the schema in `schema/neo_core_block_schema.json`
- loading it at runtime
- validating blocks with `jsonschema`
- reporting validation errors
- using natural-language parsing for repo actions
- supporting commands like commit, create folder, insert code, move or assess files

That gives the batch a proto-runtime loop:
user gives natural language → Poe interprets → asks for missing parameters if needed → validates rich blocks if applicable → acts in terminal/repo → commits work

A dual-runtime implication is present:
- strict schema-driven path for rich blocks
- looser or reduced-validation path for simple blocks

## Independent Review
This batch has high Stage 1 value because it directly confronts the gap between structured UMG artifacts and actual working agent behavior in a repo.
Its strongest contribution is not that it finishes Cantocore or settles sleeve law.
Its strongest contribution is the clear practical tension it surfaces:
a usable system likely needs both rich canonical structure and lightweight everyday authoring.

That is highly relevant to long-term UMG usability.

The second strongest contribution is the repo-operable agent pattern.
The source treats Poe not just as a concept-holder, but as a terminal/codespace actor that should:
- understand natural language
- ask clarifying questions
- read/write/move files
- restructure directories
- load schemas
- commit changes

The third strongest contribution is the explicit schema file convention.
That gives a concrete storage and validation path rather than leaving block structure purely conceptual.

Main cautions:
- Cantocore and Cyentocore definitions remain provisional
- rich schema and minimal block mode are not reconciled into one stable system
- the supplied rich schema still contains taxonomy and merge assumptions that may conflict with later canon-safe simplifications
- sleeve update logic is acknowledged but unspecified
- autonomy boundaries, commit policy, and permission model remain underdefined

## Roadmap Mapping
Primary domain: repo-operable agent workflow, dual block-schema strategy, and Cantocore implementation readiness

Roadmap phases touched:
PHASE_1_CORE_ALIGNMENT
PHASE_2_COMPILER_IMPACT
PHASE_3_DOCUMENTATION_IMPACT
PHASE_4_SKILL_ALIGNMENT
PHASE_5_PRD_AND_STAGING
PHASE_6_GITHUB_EXECUTION
PHASE_7_RELEASE_READINESS

Key phase implications:
Phase 1: raises urgent taxonomy and schema-alignment questions around Cantocore, rich blocks, simple blocks, and legacy `molt_type` assumptions.
Phase 2: supports schema loading, validation, and dual-runtime handling for rich versus minimal block workflows.
Phase 3: calls for master-key documents for Cantocore and block data/metadata.
Phase 4: strongly informs terminal-agent and repo-agent workflows for Poe.
Phase 5: supports staged implementation through an “ok for now” practical system with stronger later refinement.
Phase 6: directly supports Git/codespace and commit-oriented execution planning.
Phase 7: improves release realism by distinguishing everyday utility mode from production-grade canonical structure.

## Action Outcome
Accepted as evidence.
Frozen as a Stage 1 intake pack.
Optional compiler extract, sleeve extract, blocks/MOLT extract, canon candidates, and contradiction flags are justified because the source contains a rich schema surface, runtime validation pattern, repo-operable agent design, and unresolved tensions around schema tiers, sleeves, and autonomy.

## Recommended Next Decision
Control-room review should decide how to normalize and promote:
1. Cantocore master-key language
2. block data/metadata master-key language
3. rich versus lightweight block-mode policy
4. schema location and validation contract for repo-operable agents
5. autonomy/clarification/commit boundaries for Poe in Git-backed workflows

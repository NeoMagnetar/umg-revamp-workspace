# BATCH-180 — UMG Block Deployment Guide and Artifact Contract Review

## Batch Overview
Batch ID: BATCH-180  
Source Type: derived summary / block generation, artifact packaging, and unpack-workflow consolidation  
Working Topic: grouped JSON block bundles, unpack compatibility, stable naming, one-row-per-block generation discipline, production artifact contract  
Review Status: REVIEWED  
Disposition: ACCEPT_AS_EVIDENCE

## Source Snapshot
The source records a long production-oriented workflow for generating large UMG-compatible JSON block sets across business, web app, and chatbot domains.
The strongest recurring themes are:
- generate grouped JSON files containing many full block objects
- preserve one stable block template
- keep exact filenames predictable for terminal use
- support a fixed unpack workflow via `python scripts/unpack_blocks.py <filename>.json`
- avoid switching packaging modes
- avoid malformed JSON shapes
- preserve row-level block granularity when that is the agreed mode

The source is especially valuable because it captures practical implementation friction around schema drift, naming drift, malformed bundles, wrong counts, and inconsistent interpretation of block granularity.

## Chat-Level Summary
This batch is strongest as an artifact-contract and deployment-discipline source.
Its central contribution is the operational rule set for how UMG blocks should be generated and delivered in practice.

The strongest reusable signal is:
- one grouped JSON file
- containing a list of full block objects
- with stable names
- ready for the unpack script
- no alternate packaging unless explicitly requested

The second strongest contribution is the row-to-block rule.
The user repeatedly insisted that, when the intended pattern is “every row is a block,” the system must not collapse rows into category summaries or other reduced forms.

The third strongest contribution is runtime compatibility visibility.
The unpack script’s behavior and failure modes are treated as production reality, not afterthoughts.

## UMG-Relevant Extraction

### Core UMG Semantics
- Each listed item in a category becomes its own UMG block when that is the agreed pattern.
- UMG is operationalized as a modular encoding workflow for structured domain/category tables.
- The workflow depends on repeatability:
  - same block template
  - same output pattern
  - same unpack convention
  - same metadata style

### MOLT Roles / Taxonomy
Multiple MOLT types appear in active generation practice:
- `Instruction`
- `Subject`
- `Primary`
- `Philosophy`
- `Directive`
- `Blueprint`
- `Trigger`
- `Deployment`
- `Off`

The unpack script validates against a fixed operational taxonomy.
The source shows that role stability matters more than experimentation; arbitrary switching was not tolerated when it broke continuity.

### Priority
Priority is preserved through:
- `snap_config.stack_priority`
- ordered category progress through grouped ranges
- stable sequential workflow:
  generate file → download exact file → unpack exact file → continue

Priority therefore exists both as structural metadata and as operator workflow order.

### Merge
Merge metadata is expected inside valid block objects:
- `merge_logic.merge_as`
- `merge_logic.accepts`

A recurring accepted pattern:
- `merge_as: "instruction"`
- `accepts: ["Primary", "Blueprint", "Directive"]`

`cantocore` strings also repeatedly encode merge support, often in forms such as:
- `MERGE.SUPPORTS=PRIMARY+PHILOSOPHY+DIRECTIVE`

This batch therefore preserves merge-readiness as part of artifact structure, not just theory.

### Bundle
Accepted bundle pattern:
- one downloadable JSON file
- containing many block objects
- later unpacked into individual `.block.json` outputs

Rejected bundle patterns:
- zip files
- images
- malformed summary bundles
- category maps or strings instead of block objects

The key bundle rule is structural:
the export file must be a list of actual block objects.

### NeoBlock Composition
High-frequency accepted fields include:
- `block_id`
- `label`
- `category`
- `description`
- `molt_type`
- `cantocore`
- `snap_config`
- `merge_logic`
- `ledger`
- `display`
- `tags`
- `editable_fields`
- `example_block_data`
- `code_modules`
- `runtime_behavior_flags`
- `agent_orchestration`
- `integration_layer`
- `future_extensions`

Identity must be explicit:
- proper filename
- proper `block_id`
- proper `label`
- proper category path

The working expectation is that blocks must remain both human-readable and unpack-compatible.

### NeoStack Architecture
Stack-oriented metadata appears through:
- `SNAP.TO=STACK`
- `stack_priority`
- `supports_merge`

Blocks are expected to unpack into MOLT-specific folders for downstream builder use.
Stacking is therefore practical here, not theoretical:
generate → unpack → store by MOLT → use downstream.

### Governance / Control
The user enforced strong deterministic process governance:
- no images
- no zip files
- no unexpected mode changes
- same template every time
- same interpretation once pattern is established

Control expectations included:
- exact filenames
- exact unpack commands
- exact structural interpretation of row-to-block versus category-to-block mode

### Output Blueprint / Rendering Separation
The user repeatedly separated:
- content payload
- downloadable JSON artifact
- unpack instruction
- terminal workflow

Rendered explanation is not the artifact.
The correct delivery unit is:
- downloadable JSON file
- plus one-line unpack command

### Compiler / Runtime Logic
The unpack script is the operational import/runtime gateway in this batch.
Observed behavior:
- reads a JSON file
- expects a list of block objects
- validates `molt_type`
- writes files into `data/blocks/<molt_type>/`
- derives safe filenames from `block_id`
- skips existing files instead of overwriting

Major failure mode preserved:
- `string indices must be integers, not 'str'`
This occurred when the JSON structure was not a proper block-object array.

Runtime reality therefore requires:
- schema-valid block list
- exact filename
- importer-compatible object shape
- possibly linted counts before unpack

### Documentation / Spec Language
The user’s category tables function as raw material for documentation-to-block conversion.
Repeated spec-like conventions:
- clear category names
- short descriptions per block
- filenames reflecting category scope
- stable descriptive block IDs
- same template every time

### Skill / Agent Workflow
This is a real production workflow:
- user provides categories
- assistant generates grouped JSON
- user unpacks locally in terminal
- assistant repairs artifacts if needed

The assistant is used as part of a production toolchain, not only as a writer.

### Safety / Bounded Agency
Safety appears here mainly as bounded production behavior:
- do only the requested artifact work
- do not switch output mode
- do not improvise unrelated delivery surfaces
- preserve deterministic generation

## Independent Review
This batch has high Stage 1 value because it captures the practical artifact contract required for UMG block production.
Its strongest contribution is not new semantic theory.
It is operational discipline:
bundle shape,
filename stability,
template consistency,
row-level blockification,
and unpack compatibility.

The source is also valuable because it exposes the exact places where a production pipeline fails:
- malformed list shape
- filename drift
- wrong grouping logic
- wrong counts
- template switching

Main cautions:
- MOLT assignment across similar domains is not fully stabilized
- naming canon across grouped exports is not fully frozen
- some prior generated files were explicitly rejected and should not be treated as trustworthy canon artifacts
- row-versus-category granularity must always be made explicit
- the accepted template is inferred from repeated success rather than frozen in a single formal spec statement here

## Roadmap Mapping
Primary domain: production artifact contract, unpack compatibility, and deterministic block generation

Roadmap phases touched:
PHASE_1_CORE_ALIGNMENT
PHASE_2_COMPILER_IMPACT
PHASE_3_DOCUMENTATION_IMPACT
PHASE_4_SKILL_ALIGNMENT
PHASE_5_PRD_AND_STAGING
PHASE_7_RELEASE_READINESS

## Action Outcome
Accepted as evidence.
Frozen as a Stage 1 intake pack.
Optional compiler extract, blocks/MOLT extract, canon candidates, and contradiction flags are justified because the source contains a strong artifact contract, importer/runtime behavior, practical taxonomy usage, and repeated failure cases that matter for tooling canon.

## Recommended Next Decision
Control-room review should decide how to normalize and promote:
1. formal artifact contract for grouped JSON bundles
2. canonical row-versus-category blockification rules
3. canonical grouped-file naming conventions
4. importer lint/QA requirements before unpack
5. stable operational template for production block generation

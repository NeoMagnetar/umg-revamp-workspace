# BATCH-106_BLOCK_REORGANIZATION_AND_SCHEMA_ENFORCEMENT_REVIEW

## Batch Overview
- **Batch ID:** BATCH-106
- **Short Topic:** block reorganization and schema enforcement
- **Source Type:** Derived extraction / handoff note, not raw transcript
- **Review Status:** REVIEWED
- **Disposition:** ACCEPT_AS_EVIDENCE
- **Primary Domain:** metadata-driven block routing, schema enforcement, and repository recovery workflow
- **Confidence Note:** This batch is highly operational. It captures a real repository reorganization attempt, a metadata-driven routing failure, schema-validation fallout, and the interaction between repository tooling, Git hygiene, and runtime readiness. Its value is strongest as evidence for compiler/documentation hardening rather than as settled canon.

## Source Snapshot
- Source title: `106 block reorganization and schema enforcement`
- Source character: summarized extraction of a troubleshooting and repository-repair chat
- Main themes surfaced by source:
  - reorganizing 2000+ `.block.json` files into `data/blocks/<Category>/<MoltType>/`
  - Python script workflow for dry-run planning, execution, and verification
  - metadata collapse into `Misc` because of schema/metadata issues
  - large Git operations, merge conflicts, rebases, force pushes
  - GitHub push protection blocking exposed secrets
  - history rewrite using `git filter-repo`
  - validation errors in block schema and content typing
- Provenance caution:
  - source is a distilled extraction note rather than the raw logs and scripts
  - validator output is referenced but not fully reproduced here
  - final canonical schema policy still remains unresolved

## Chat-Level Summary
This batch contributes a concrete repository-scale reorganization packet for UMG blocks. It shows that filesystem structure is being derived from declared block metadata rather than file names, and that missing or malformed metadata can collapse thousands of blocks into fallback buckets like `Misc/Unknown`. It also captures a proto-compiler workflow: dry-run planning, execution, verification, validation, and release-style checkpointing. The packet is unusually valuable because it ties semantic integrity directly to operational integrity: bad metadata breaks folder routing, schema mismatch breaks validation, and secret leakage breaks release operations. The batch therefore pressures clearer canonical metadata rules, a single source-of-truth reorg script, stronger normalization logic, validation gates, and safer staging/release discipline.

## UMG-Relevant Extraction
### Core semantics
- Blocks are `.block.json` units whose runtime/storage placement is derived from internal metadata such as `category` and `molt_type`.
- File naming alone is not authoritative for block organization.
- Incorrect or missing metadata causes fallback routing to generalized buckets.
- Validation is treated as a structural enforcement mechanism for block integrity.

### MOLT / taxonomy signal
- `molt_type` is used operationally to derive subfolder placement.
- Canonical hierarchy is implied as:
  - Category → MoltType
- Taxonomy drift or mismatch directly degrades organization quality and downstream usability.

### Merge / schema pressure
- `merge_logic` appears in repository blocks but is rejected by the validator.
- This suggests unresolved tension between intended merge semantics and the currently enforced schema.
- Schema drift is not abstract here; it is directly visible in validation failures.

### NeoBlock composition signal
- Canonical structural pressure appears around:
  - `category`
  - `molt_type`
  - `content`
  - `merge_logic`
  - `export_config`
  - `color`
- `content` is expected by the validator to be an array, but many blocks use string form.
- Unexpected fields are rejected rather than normalized.

### Runtime / compiler signal
- Python reorg scripts act as proto-compilers:
  - read block metadata
  - plan target paths
  - execute moves
  - verify results
  - validate resulting repository state
- Dry-run versus execute behavior mirrors compile-planning versus compile-application stages.
- Validation acts as a post-transform type-check layer.
- Failure mode is concrete: bad metadata normalization causes large-scale category collapse.

### Governance / control signal
- Schema validation acts as internal enforcement.
- GitHub secret scanning acts as external enforcement.
- Pre-commit enforcement is implied as desirable future control.
- Repository safety and runtime readiness are intertwined.

### Output / structure separation signal
- Raw block JSON is distinct from the rebuilt runtime-ready file hierarchy.
- Scripts operate as transformation layers between storage state and consumable structure.
- Validation logs surface enforcement reality rather than design intention.

### Documentation / release signal
- The batch strongly pressures documentation for:
  - canonical allowed fields
  - category normalization rules
  - `content` type requirements
  - merge-field policy
  - canonical reorg pipeline
- Tagging and backup/reorg checkpoints imply release-like staging discipline.

## Independent Review
This batch is best treated as a **repository-normalization and enforcement packet**. Its importance is broader than just fixing a folder tree. It shows that UMG’s structural integrity depends on reliable declared metadata, not just conceptual architecture. When metadata, schema, and tooling drift apart, the result is not merely cosmetic disorganization; it disrupts validation, downstream consumption, and release confidence.

The batch also connects UMG work to practical repository operations. It shows that the block ecosystem needs stronger operational doctrine: one canonical reorg tool, a documented normalization strategy, a clear validator contract, and staging gates that catch both schema drift and secret leakage before release actions occur.

The main unresolved question is policy. The packet does not settle whether the schema should evolve to match repository reality or whether the repository should be migrated to fit a stricter standard. That decision will affect compatibility, migration cost, and how aggressively UMG can standardize block composition going forward.

## Roadmap Mapping
### PHASE_1_CORE_ALIGNMENT
- pressures clarification of:
  - canonical metadata fields for block placement
  - whether merge-related fields are allowed at block level
  - how strict category and `molt_type` normalization should be

### PHASE_2_COMPILER_IMPACT
- pressures need for:
  - one canonical reorg tool
  - metadata normalization before routing
  - validation after transform
  - migration tooling for schema drift
  - explicit handling of unknown fields and type mismatches

### PHASE_3_DOCUMENTATION_IMPACT
- suggests documentation on:
  - category → MoltType hierarchy
  - allowed field list
  - `content` array requirement
  - normalization aliases/case rules
  - repository reorg and validation workflow

### PHASE_4_SKILL_ALIGNMENT
- suggests:
  - reusable validation/audit utilities
  - a canonical `reorg_blocks.py` or equivalent workflow skill
  - agent guidance for plan → execute → validate → commit loops

### PHASE_5_PRD_AND_STAGING
- suggests:
  - backup → dry-run → execute → validate → commit/tag staging pattern
  - pre-commit secret scanning and validation enforcement
  - documented rollback / checkpoint practices for large repo transforms

## Action Outcome
- **Disposition chosen:** ACCEPT_AS_EVIDENCE
- **Why:** the batch is strongly grounded in real operational failure and recovery patterns, but it does not settle the canonical schema or normalization policy.
- **Optional extracts justified:**
  - `COMPILER_EXTRACT` because the source strongly pressures normalization, routing, validation, and staging logic.
  - `BLOCKS_MOLT_EXTRACT` because the source clarifies metadata-driven block placement, schema-field pressure, and repository composition drift.

## Recommended Next Decision
Decide whether UMG block routing should rely on a strict canonical metadata contract with migration tooling, or a more permissive normalization layer that tolerates legacy fields and aliases during repository reorganization.

# BATCH-147 — Compiler Extract

## Scope
Compiler- and generation-pipeline implications extracted from the block-production source.

## High-Value Compiler Claims
1. A generator can convert category tables into standardized UMG JSON block files using a repeated schema.
2. The schema currently includes:
   - `block_id`
   - `label`
   - `category`
   - `description`
   - `editable_fields`
   - `molt_type`
   - `tags`
   - `canto_overlay`
   - `ledger`
   - `trigger`
   - `export_config`
3. `category` is treated as path-aware rather than purely descriptive.
4. `block_id` is provisional and intended for later finalization/hashing.
5. `trigger` exists in the schema even when null.
6. Future schema expansion may include `function_calls` and AI instructions.
7. Folder and zip production are first-class outputs of the workflow, not incidental byproducts.

## Likely Compiler Audit Targets
Canonical schema field guarantees.
`block_id` finalization and hashing policy.
Default MOLT role assignment policy.
Null-trigger handling and future trigger activation rules.
Path normalization and filename sanitization.
Zip packaging conventions across subcategories.

## Risk Surface
Any later system that ignores the path-aware schema and packaging discipline shown here would lose a major operational advantage.
Any assumption that null-trigger batch output already proves trigger semantics are solved would overstate the evidence.

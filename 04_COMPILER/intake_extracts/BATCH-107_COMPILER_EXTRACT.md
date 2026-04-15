# BATCH-107 — Compiler Extract

## Compiler / Validation Signal
This batch contains strong evidence that UMG block-builder recovery depends on a strict validation-and-normalization layer before any reorganization or builder execution is attempted.

## Concrete Script Surfaces
- `scripts/validate_blocks.py`
- `scripts/autofill_block_fields.py`
- `scripts/block_builder.py`

## Observed Validation Expectations
- recursive scan over `data/blocks/**/*.block.json`
- Draft7 JSON Schema validation
- explicit path-based error reporting
- strict required-field enforcement
- strict additional-property rejection
- content-shape enforcement via `oneOf(prompt_template | body)`

## Observed Patch / Normalization Expectations
- strip legacy keys not allowed by schema
- normalize `molt_type`
- fill required defaults
- convert legacy content forms
- normalize `editable_fields`
- convert `code_modules[].path` to `code`

## Strong Compiler Tasks Implied
1. **Canonical validator**
   - one validator surface for all blocks
   - deterministic error reporting
   - fail-fast or report-all mode
2. **Canonical patcher**
   - migrate legacy blocks into schema-valid forms
   - make provisional transformations explicit in logs
3. **Canonical generator**
   - create valid blocks before they enter the library
   - validate at creation time, not only after drift
4. **Routing preprocessor**
   - normalize category / subcategory / MOLT fields before folder placement
5. **CI gate**
   - block drift before merge or release

## Direct Compiler Risks
- unresolved `domain` status means compiler target schema is not fully locked
- unresolved `Deployment` handling means role normalization is provisional
- unresolved manifest/unpack instability means downstream generation paths are not yet stable
- strict schema may reject conceptually useful fields unless canon and schema are reconciled

## Recommended Compiler Decision Target
Freeze one canonical builder data contract, then align:
- validator
- patcher
- generator
- reorg logic
- CI gate
against that contract with no parallel variants.

# BATCH-177 — Compiler Extract

## Scope
Compiler- and runtime-facing implications extracted from the Poe repo-integration source.

## High-Value Compiler Claims
1. Rich blocks should be validated against a repo schema file located at `schema/neo_core_block_schema.json`.
2. Runtime should be able to load the schema and validate blocks using `jsonschema`.
3. The agent loop should support:
   - natural-language parsing
   - parameter clarification
   - repo file operations
   - folder creation
   - code insertion
   - commit actions
4. The source strongly implies dual validation/runtime modes:
   - strict schema-driven mode for rich blocks
   - reduced or looser handling for lightweight everyday blocks
5. Trigger, merge, snap, stack, provenance, and code modules all appear as supported surfaces in the richer schema.
6. The richer schema includes recursive block composition and embedded code modules.

## Likely Compiler Audit Targets
Schema tier policy.
Rich versus minimal block validation strategy.
Runtime schema-loading path.
Natural-language command parsing contract.
Parameter-clarification thresholds.
Commit and file-operation safety policy.
Migration path from lightweight blocks into richer canonical blocks.

## Risk Surface
Any implementation that forces every daily block through the full rich schema may become unusable.
Any implementation that abandons schema validation entirely will lose one of the strongest structural controls surfaced in this batch.

# BATCH-197 - Blocks and MOLT Extract

## Scope
Block- and typed-structure signals extracted from the language-layer source.

## Explicit Typed Usage Preserved
The source uses `molt_type` as an explicit field in machine-readable examples.

Examples preserved:
- `molt_type: Subject`
- `molt_type: Blueprint`

## Structural Signal
This reinforces that MOLT roles can appear as explicit typed fields inside machine-readable block structures.

## Example Block Surface
The `daily_stock_report` example includes:
- inputs / requires
- outputs / produces
- snap target
- description / label / category
- tags
- ledger/provenance-like fields in NeoCore form

## Important Caution
This batch supports typed field usage, but does not develop hierarchy, trigger, priority, or merge law.

# BATCH-106_BLOCKS_MOLT_EXTRACT

## Scope
MOLT / block-role / candidate-block signals extracted from BATCH-106.

## Canonical Routing Pressure
The batch strongly reinforces that blocks are routed by declared metadata, not by filename or current path.

High-value structural pressure:
- `category` determines top-level placement
- `molt_type` determines subfolder placement
- missing or malformed metadata collapses blocks into fallback buckets
- normalization must happen before routing

## Composition Drift Signal
The source highlights recurring field-level problems:
- `content` uses string form where validator expects array
- `merge_logic` appears in blocks but is rejected
- additional fields such as `color` and `export_config` trigger errors

This indicates that block authoring practice and canonical schema are not fully aligned.

## MOLT / taxonomy signal
Operationally, `molt_type` is functioning as a routing taxonomy. That means taxonomy consistency is no longer just documentation; it directly affects repository organization and downstream block discoverability.

## Merge pressure
`merge_logic` is especially important because:
- it exists conceptually in UMG
- it exists in repository data
- it may not exist in the enforced schema

This makes it a high-priority reconciliation target between design intent and implementation reality.

## Workflow Signal
The reorganization pipeline implies a candidate durable pattern:
- flatten or ingest block inventory
- normalize metadata
- route to canonical hierarchy
- validate structure
- checkpoint stable state

## High-Value Documentation Targets
- blocks are placed by declared metadata, not by filename or path
- document canonical `category` and `molt_type` values
- document fallback behavior for invalid metadata
- define `content` type expectations clearly
- resolve whether `merge_logic` is canonical, extension-only, or disallowed

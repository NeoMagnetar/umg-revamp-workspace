# BATCH-113 — Compiler Extract

## Ingestion/runtime-facing signal
This batch proposes a deterministic transcript-ingestion and artifact-extraction pipeline that could act as a compiler-adjacent evidence-processing layer for the project.

## Strong candidate pipeline
1. normalize
2. segment
3. extract artifacts
4. version + lineage
5. index
6. conflict-detection pass
7. persist
8. render report/PDF

## Typed emission rules surfaced
- emit `definition` when a term-to-meaning statement appears
- emit `umg_rule` when a prescriptive constraint appears
- emit `sleeve` / `block` when IDs or structural configuration appear
- emit `json_or_code` for fenced or JSON-like material
- emit `analysis` for claims + methods + outputs
- preserve ambiguous material as `candidate`

## Conflict engine signal
### Proposed conflict classes
- definition conflicts
- UMG rule conflicts
- sleeve conflicts
- block conflicts
- terminology drift conflicts
- authority conflicts
- constraint violations

### Proposed severities
- critical
- high
- medium
- low

### Proposed auto-resolution methods
- supersede
- scope split
- rename
- merge
- governance override
- priority select
- manual note
- dismiss

## Data model pressure
The archive object model stores:
- archive metadata
- chats
- turns
- artifacts
- conflicts

This suggests a persistent evidence layer that can support:
- synthesis
- contradiction tracking
- report generation
- later control-room promotion decisions

## Candidate tasks
- define canonical artifact IDs and conflict IDs
- define required vs optional fields per record type
- define normalization and segmentation rules
- define confidence handling and `candidate` status behavior
- define persistence target (repo JSON, SQLite, Airtable, other)
- define transcript-to-report renderer contract

## Caution
Do not silently treat the proposed schema, scope model, or resolution methods as canon until the project explicitly ratifies them. This batch is strongest as workflow infrastructure evidence.

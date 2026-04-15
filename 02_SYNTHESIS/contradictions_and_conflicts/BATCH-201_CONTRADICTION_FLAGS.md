# BATCH-201 — Contradiction / Ambiguity Flags

## Contradiction Watch
HIGH

## Main Flags
### 1. `Deployment` Status
`Deployment` appears in folders, docs, manifests, and autoblocks, but its exact canonical role remains unresolved.

### 2. `Merge` Status
`Merge` remains listed in schema reference yet is questioned in runtime logic as possibly non-canonical or operation-like.

### 3. Manifest vs Stack vs Schema Confusion
The distinction among builder manifests, stack JSONs, and schema matrices was still causing naming and placement confusion.

### 4. `webMatrix.json` Role
Its relationship to former website-build stack semantics and builder schema was still somewhat confusing during migration.

### 5. Sleeve Boundary
`/poe_core/sleeves/` versus `/sleeves/` was partially clarified but not yet institutionalized as a formal canon distinction.

### 6. Poe Builder Bridge
Poe integration inside the web builder is clearly desired, but the final bridge architecture was not chosen.

## Intake Conclusion
Use this batch for:
- repo structure docs
- schema/runtime reconciliation
- builder migration planning
- Poe integration planning

Do not use it alone to settle:
- final `Deployment` canon status
- final `Merge` canon status
- final builder/Poe bridge architecture
- final long-term bundled export strategy

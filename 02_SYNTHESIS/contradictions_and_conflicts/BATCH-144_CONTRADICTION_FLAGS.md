# BATCH-144 — Contradiction Flags

## Scope Note
These are not canon decisions.
They are tensions or possible conflicts surfaced by the source.

## Flag 1
**Topic:** Replaced categories 21–28  
**Tension:** Earlier conceptual categories and later control/safety/expansion categories both exist in the history.  
**Why it matters:** Reconciliation is needed before treating the late categories as fully canonical.

## Flag 2
**Topic:** Builder completeness mismatch  
**Tension:** Business builder and webapp builder outputs were not equally complete when artifacts were produced.  
**Why it matters:** Serialization success in one builder domain should not imply completeness across all domains.

## Flag 3
**Topic:** Local merge/conflict rules  
**Tension:** Merge/conflict logic appears in specific places such as injection, persona switching, or local policies, but not as a globally unified rule system.  
**Why it matters:** Runtime predictability will require stronger normalization.

## Flag 4
**Topic:** Runtime versus compile-time blur  
**Tension:** Instruction injection, persona switching, and memory editing behave like runtime modification, while JSON/zip packaging suggests compile-time serialization.  
**Why it matters:** The project needs a cleaner distinction between build-time and run-time layers.

## Flag 5
**Topic:** Missing schema versioning  
**Tension:** The builder pattern is strong, but there is no fully formal schema-versioning system across domains.  
**Why it matters:** Portable multi-domain builders need clearer version governance.

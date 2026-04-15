# BATCH-131 — Compiler Extract

## Scope
Compiler-boundary and Studio-integration implications extracted from the source.

## High-Value Compiler Claims
1. Studio must compile exactly the Active Sleeve model shown in Right Panel input JSON.
2. Compile is explicit via a Compile button; no auto-compile in v1.
3. Layout metadata is required for Studio UI but ignored by compiler semantics.
4. Compiled sleeve file format should include sleeve data, layout, compile outputs, and hashes.
5. Sleeve hash should be computed over canonicalized sleeve excluding layout.
6. Runtime hash should be computed over canonicalized RuntimeSpec.
7. Governance in v1 is scoped to NeoStack-level peer conflict resolution and priority override.
8. Governance may not change MOLT type, reorder raw blocks within a column, or create composition operations.
9. Bundle and merge replacement semantics should not leave original siblings duplicated beside the resulting composite artifact.
10. Same-MOLT restriction for bundle and merge is a deliberate v1 simplification to preserve deterministic Studio behavior.
11. Stats/Hash surfaces should expose counts, conflict reports, compile metadata, and hashes.

## Likely Compiler Audit Targets
Compiled sleeve import/export schema.
Hash canonicalization rules.
Governance override ordering.
Same-MOLT enforcement for Studio-issued bundle/merge operations.
Replacement semantics for bundle and merge.
Boundary between Studio layout state and compiler-consumable structure.
Right-panel Runtime/Trace/Raw contract consistency.

## Risk Surface
Any Studio implementation that lets graph gestures silently mutate compiler semantics would conflict with this batch.
Any implementation that treats layout metadata as semantic compiler input would conflict.
Any v1 implementation that re-expands governance into global or raw-block mutation without explicit redesign would conflict.

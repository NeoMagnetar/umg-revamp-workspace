# BATCH-107 — Contradiction Flags

## Contradiction / Tension Summary
This batch contains multiple unresolved tensions that should not be silently normalized into canon.

## Flag 1 — `domain` in schema vs folder-only organization
- `domain` appears as a proposed required field in schema v2.0.
- The user explicitly questions whether domain is already represented structurally through the top-level major groupings and subcategories.
- Operationally, `domain` was introduced, questioned, and partially removed to keep older validation green.
- **Status:** unresolved

## Flag 2 — `Deployment` as a main MOLT type
- Legacy data used `Deployment`.
- Repair scripts normalized it to `Instruction`.
- The user explicitly stated discomfort with `Deployment` as a main MOLT role.
- **Status:** unresolved, with operational workaround but no semantic decision

## Flag 3 — category browsing vs MOLT runtime semantics
- The batch strongly distinguishes browsing taxonomy from runtime role.
- At the same time, reorg and builder recovery work depends on both.
- Without an explicit control-room rule, folder organization can accidentally be treated as semantic logic.
- **Status:** unresolved but directionally clarified

## Flag 4 — strict schema vs practical legacy tolerance
- Working schema is strict (`additionalProperties: false`).
- Legacy data includes many nonconforming keys and shape variants.
- This creates a live conflict between repository reality and validator expectations.
- **Status:** unresolved; migration strategy not frozen

## Flag 5 — canonical script surface drift
- Multiple scripts and names appear during recovery:
  - `fix_blocks.py`
  - `autofill_block_fields.py`
  - `unpack_blocks.py`
  - `block_builder.py`
- No single source-of-truth script surface was finalized in the source.
- **Status:** unresolved operational drift

## Flag 6 — manifest/unpack instability
- Manifest regeneration and unpack logic were not stabilized.
- Builder data-layer recovery advanced farther than manifest flow stabilization.
- **Status:** unresolved

## Immediate Synthesis Risk
If these contradictions are not explicitly resolved, future builder restoration may hard-code provisional repair behavior as if it were canon.

## Recommended Next Decision Target
Create one control-room decision bundle covering:
1. canonical schema surface,
2. canonical role surface,
3. canonical migration surface,
4. canonical folder/routing surface.

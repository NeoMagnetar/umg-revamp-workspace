# BATCH-136 — Contradiction Flags

## Scope Note
These are not canon decisions.
They are tensions or possible conflicts surfaced by the source.

## Flag 1
**Topic:** `merge_logic` on an Instruction block  
**Tension:** The block includes `merge_logic: instruction_overrides_subject`, which may encode authority assumptions at the block level.  
**Why it matters:** Broader canon may prefer that authority and interaction laws live outside individual content blocks.

## Flag 2
**Topic:** UI/display fields mixed with semantic fields  
**Tension:** `display` and `snap_config` are bundled into the same artifact as semantic content.  
**Why it matters:** The project needs a stable separation between semantic block law and renderer/editor metadata.

## Flag 3
**Topic:** Ledger automation field  
**Tension:** `created_at: AUTO` implies auto-populated provenance behavior without a locked standard for where and when that population occurs.  
**Why it matters:** Provenance handling should be explicit across compiler, storage, and frontend layers.

## Flag 4
**Topic:** Empty extension arrays  
**Tension:** Arrays such as `code_modules`, `runtime_behavior_flags`, and `future_extensions` are present but empty.  
**Why it matters:** The project needs a decision on whether empty extensibility surfaces belong in canonical artifacts or only in implementation storage models.

## Flag 5
**Topic:** Category metadata versus MOLT semantics  
**Tension:** `category: Software.Versioning` is useful organizationally but may not be part of core semantic law.  
**Why it matters:** Taxonomy/grouping metadata should be placed consistently across the project.

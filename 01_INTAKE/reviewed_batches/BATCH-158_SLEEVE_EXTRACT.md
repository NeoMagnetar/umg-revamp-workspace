# BATCH-158 — Sleeve Extract

## Sleeve / Overlay Material

### Explicit Sleeve Identity
- SLEEVE.POE.SUN_TZU.REFLECTIVE2_1

### Active Sleeve / Overlay Configuration
- ACTIVE_SLEEVE includes:
  - SLEEVE.POE.SUN_TZU.REFLECTIVE2_1
  - CEL_ACTIVE

### Additional Overlays
- CHAOS_LENS
- CEL_ACTIVE
- EMPTY_PATCH

### Behavioral / Style Biases
The source associates sleeves/overlays with runtime modifiers such as:
- strategic-minimal
- prefer_short_plans
- verify_often
- planner prefix
- actor prefix
- propose alternates on failure
- prefer tool calls

### Hot-Patch Surface
- EMPTY_PATCH is reserved for hot-patch conditions
- note: “They changed something”

## Interpretation
The source treats sleeves and overlays as modular runtime configuration surfaces rather than hardcoded execution logic. This supports a future resleeving/config-driven runtime model, although no final arbitration or resleeving protocol is defined here.

## Stage 1 Note
This material is evidence for sleeve/config architecture only. It should not be promoted into canon without cross-batch synthesis and normalization.

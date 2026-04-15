# BATCH-169 — Compiler / Runtime Extract

## Why this extract exists
This source repeatedly crosses from ontology into concrete runtime/compiler work. fileciteturn19file0

## Preserved Runtime / Compiler Tasks
- rename `cantocore` → `canto_overlay`
- rename `merge_logic` → `merge_behavior`
- unify sleeve loader into `src/sleeve_manager.py`
- consolidate scattered `fill_*` scripts
- validate blocks with richer schema logic
- repair command registry with `repair_registry.py`
- use `command_registry.json` for dispatch
- future `merge.ts` / shared merge engine for UI and CLI. fileciteturn19file0

## Preserved Runtime Concepts
- Trigger blocks as runtime activation units
- Deployment blocks as runtime/environment-specific overrides
- `runtime_behavior_flags`
- `memory/active_state.json` as live sleeve-state target
- import/export cycle shared between UI and backend workflows

## Main Intake Interpretation
This batch implies that UMG blocks are not just data objects. They are intended to be directly loadable runtime units with:
- schema-checked fields
- executable or dispatchable semantics
- visible merge and trigger behavior
- portable import/export representation

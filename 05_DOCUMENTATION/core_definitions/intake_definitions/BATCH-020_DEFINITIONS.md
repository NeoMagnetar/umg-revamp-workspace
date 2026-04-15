# BATCH-020 — Definitions Extract

## Terminology
### UMG_ENVOY_Resleever
Private single-agent homebase repo and OpenClaw workspace skill for storing, compiling, and switching UMG runtime assets.

### Source assets
Canonical authored materials such as sleeves, MOLT blocks, NeoBlocks, NeoStacks, and manifests.

### Compiled outputs
Derived runtime artifacts produced by compiler-aware workflows, such as compile output, runtime specs, or OpenClaw-facing config files.

### Active runtime state
The currently selected sleeve/stack state and related live control artifacts, represented explicitly rather than inferred.

### Homebase
A persistent private repo/skill surface where one agent manages its own sleeves, blocks, compiler assets, and runtime posture over time.

## Role Language
- MOLT blocks = stored atomic asset layer
- NeoBlocks = compiled or bundled higher-order units
- NeoStacks = domain-level runtime assemblies
- sleeves = runtime identity layer
- active_sleeve / active_stack = explicit current-state controls

## Architecture Language
- specification-first
- technology-agnostic framework
- source of truth
- private single-agent homebase
- compiler-aware scaffold
- workspace skill
- local clone plus GitHub sync

## Runtime / Compiler Language
- active-sleeve.json
- active-stack.json
- runtime/compile-output/
- runtime/traces/
- compile-runtime script
- local_repo_asset compiler mode
- preserve source assets
- avoid destructive overwrite

## Definitional Candidates
- “UMG is specification-first, not execution-first.”
- “Stabilize one agent first.”
- “Keep source assets separate from compiled outputs.”
- “This repository is the private UMG homebase for one OpenClaw agent.”

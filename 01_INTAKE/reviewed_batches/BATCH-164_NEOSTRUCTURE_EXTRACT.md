# BATCH-164 — NEOSTRUCTURE EXTRACT

## Implied Structural Stack
### Data Layer
Datasets and normalized chat examples.

### Block Layer
Alignment, MOLT, and overlay JSON blocks.

### Engine Layer
Training code and inference wrapper logic.

### Config Layer
Training and evaluation configuration files.

## Runtime Composition
base model + LoRA adapter + overlay + alignment guard

## Repo Boundary Signal
The source formalizes system boundaries through folders such as:
- vault
- blocks
- engine
- configs
- scripts

## Architectural Value
This is useful evidence for a UMG-compatible ML architecture because it preserves clean boundaries between:
- learned behavior
- governed behavior
- rendered behavior
- operational code
- configuration

## Limits
NeoStack logic is implied rather than explicitly canonized.

# BATCH-164 — COMPILER EXTRACT

## Compiler / Preprocessing Signal
The batch treats data preparation as a deterministic transform:
raw examples → MOLT-normalized chat format → training dataset

## Runtime Signal
The batch describes a runtime chain:
generate → alignment guard → overlay transform

## Concrete Compiler / Runtime Candidates
- raw dataset → normalized chat transformer
- assistant-only training collator
- post-generation overlay pipeline
- guarded inference wrapper
- config-driven evaluation and deployment logic

## Important Open Issues
- Overlay vs learned behavior precedence is unresolved.
- Alignment is duplicated between training data and inference guard.
- MOLT augmentation fields are named but not fully enforced by the training loop.
- The collator relies on a delimiter that may not match the dataset format.

## Stage 1 Holding Position
Use this batch as evidence for compiler/runtime planning, especially for:
- preprocessing standards
- inference pipeline order
- alignment hierarchy
- schema validation

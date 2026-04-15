# BATCH-164 — DEFINITIONS

## UMG
A modular cognition system whose parts can be swapped or combined without breaking the whole.

## MOLT
Used here as a structured prompt/template scaffold for normalizing training data into consistent chat format.

## ALIGNMENT block
A JSON-defined block carrying refusal rules, honesty requirements, creed, or governance instructions applied during training and/or inference.

## MOLT template block
A structured schema block that defines message roles and augmentation fields used to normalize examples.

## OVERLAY block
A structured post-generation modifier that alters presentation or output framing without changing model weights.

## Block
A modular JSON configuration unit loaded independently rather than embedded invisibly in prompt text.

## LoRA adapter
The trained fine-tuning artifact layered on top of a base model.

## Alignment guard
An inference-time control function that checks or modifies model output to enforce governance.

## style_overlay
An augmentation field referenced in the source as part of MOLT normalization, likely affecting expression rather than base semantics.

## checklist
An augmentation field referenced in the source, here exemplified by UNDERSTAND / REFLECT / REFINE.

## Blueprint separation
The separation between learned model behavior and runtime output shaping or overlay rendering.

## Training pipeline
The sequence prepare data → fine-tune → evaluate → deploy.

## Repo architecture
The organized boundary between vault/blocks, engine code, configs, and scripts.

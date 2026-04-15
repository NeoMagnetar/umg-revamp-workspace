# BATCH-083 — Compiler / Runtime Extract

## Scope
This extract captures the strongest compiler/runtime surfaces preserved in the batch.

## Source-Backed Points
- A UMG preamble is described as injected before model calls.
- Logic is interpreted through a hierarchy of blocks including Primary, Subject, Merge, and Instructions.
- Priority toggles are defined as:
  - 0 = Off
  - 1 = Primary
  - 2 = Secondary
  - 3 = Tertiary
- Token weights are mapped to priority state.
- Merged blocks can share the same toggle number.
- Merged blocks execute in order of priority; unassigned blocks are ignored.
- A block merge engine is described as:
  - merging blocks into prompt stack
  - handling hierarchy and priority logic
  - contributing to tokenizer estimate / payload building
- The long whitepaper surface describes an engine flow of:
  - user assembly
  - preparation/orchestration
  - generation
  - review/iteration
- The self-adaptive surface adds:
  - pre-response build using active MOLTs
  - post-response weight adjustment based on feedback

## Compiler / Runtime Pressure
This batch is significant because it preserves one of the clearer execution models seen in the intake stream:
- block hierarchy
- priority-based execution
- token weighting
- merge engine
- preamble injection
- optional post-response adjustment

## Conservative Intake Reading
Useful for:
- compiler audit log seeds
- priority/task extraction
- runtime normalization questions
- merge-engine implementation notes

Not enough to:
- settle final compiler canon
- settle full merge law
- settle exact token model
- settle how self-adaptive behavior fits core versus extension

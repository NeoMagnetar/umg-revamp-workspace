# BATCH-028 — Blocks and MOLT Extract

## Core Blocks/MOLT Signal
- NeoBlocks should be built from known canonical MOLT atoms already stored in project files.
- Future draft examples should stop inventing trigger numbers when canonical trigger blocks already exist.
- Canonical ID reuse is treated as part of architectural reliability, not just naming style.

## Composition Pattern
- structural hierarchy:
  - Block
  - NeoBlock
  - NeoStack
  - Sleeve
- routing chain:
  - Trigger
  - Neostack
  - Directive
  - Instruction
  - Execution
  - Verify
  - Report

## Practical Implication
- Draft neostacks may remain useful structurally even when their identifiers are not yet normalized.
- A structurally good example is not automatically a compiler-ready example.
- Blocks/MOLT work should preserve composition style while swapping invented IDs for canonical references.

## Candidate Follow-On Review
- compare current OpenClaw neostack examples against actual MOLT inventory
- identify which trigger references are placeholders
- normalize example IDs before treating examples as reusable canonical patterns

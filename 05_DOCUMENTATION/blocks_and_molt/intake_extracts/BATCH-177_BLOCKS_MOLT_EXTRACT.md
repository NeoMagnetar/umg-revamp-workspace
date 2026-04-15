# BATCH-177 — Blocks and MOLT Extract

## Scope
Block- and MOLT-structure signals extracted from the repo-agent/schema source.

## MOLT Types Present in Supplied Schema
- Primary
- Subject
- Instruction
- Directive
- Philosophy
- Blueprint
- Merge
- Trigger
- CodeBlock
- Off

## Important Note
This schema preserves a broader or older taxonomy surface than some later compiler-tightened canon work.
That makes it valuable evidence, but not automatically final canon.

## Structural Signals
- `molt_type` is required
- block identity is anchored partly by molt role/type
- rich blocks can be recursive
- simpler everyday blocks still preserve `molt_type` even when other metadata is omitted

## Dual Block Philosophy
The source strongly implies two operating modes:
- rich metadata-heavy blocks
- lightweight practical blocks

This is one of the most important design tensions in the batch.

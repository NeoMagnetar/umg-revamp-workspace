# BATCH-072 Blocks / MOLT Extract

## Core Distinction
- **MOLT Block Types** were treated as structural categories of thought blocks.
- **Block Roles** were treated as functional jobs performed inside a stack.
- The source explicitly places block types in **framework** documentation and roles in **glossary** documentation.

## Extracted Block Language
### Structural / framework-facing
- MOLT Block Types
- Snap
- Merge
- Stack

### Functional / role-facing
- Primary
- Subject
- Philosophy
- Term

## CyentCore Compact Block Syntax
- `BLOCK:Primary("UMG.Chat.Audit")`
- `BLOCK:Subject("Transcript: <<id>>")`
- `BLOCK:Philosophy("Strict-Context; Evidence-First; Modular-Comparative")`
- `BLOCK:Term("...")`

## Implications
- The batch strengthens the need to separate architecture terms from role/job terms in UMG documentation.
- Compact block emission is treated as a practical output syntax for audit findings.
- The source supports later work on NeoBlock composition rules, but does not finalize them.

## Open Questions
- Are CyentCore block lines part of canonical UMG syntax, or only a compact audit/reporting notation?
- Should Snap / Merge / Stack be documented as verbs, block types, engine phases, or all three?
- How should block-type documentation reference role definitions without collapsing the distinction?

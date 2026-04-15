# BATCH-049 — Blocks and MOLT Extract

## Block-Layer Findings
- MOLT roles are treated as canonical semantic atoms:
  - Trigger
  - Directive
  - Instruction
  - Subject
  - Primary
  - Philosophy
  - Blueprint
- NeoBlocks sit above MOLT atoms as grouped functional units.
- The batch supports a flexible but still structured use of MOLT fields per NeoBlock.

## High-Value Block/MOLT Signals
- Domain -> Intent -> Atomic alignment with NeoStack -> NeoBlock -> MOLT Atom
- requirement expectations for block completeness
- explicit trigger-driven activation and routing logic
- blocks used as explanatory and compiler-relevant primitives rather than only prose labels

## Risks
- full block details are not visible for all referenced artifacts
- some block sets appear generated conversationally without compile validation
- MOLT flexibility is a strength, but it increases validator design importance

## Recommended Follow-up
- verify canonical block requirements against project source files
- clarify minimum viable NeoBlock-to-MOLT completeness rules
- document when one vs multiple MOLT entries per role are valid

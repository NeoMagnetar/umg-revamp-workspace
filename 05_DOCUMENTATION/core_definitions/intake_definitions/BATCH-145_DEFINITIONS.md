# BATCH-145 — Definitions Extract

## Terminology Scope Note
These definitions are extracted from a derived metadata-policy and builder-UX summary.
They remain Stage 1 evidence until explicitly promoted elsewhere.

## Core Block Terms
**Block Metadata Policy**  
Formal policy surface defining what structured fields a block should expose and how those fields behave in UI, runtime, attribution, and export contexts.

**MOLT Lexicon HUD / View MOLT**  
Proposed builder inspector surface that reveals the UMG/MOLT meaning of a block and its fields without collapsing normal user-facing simplicity.

**CantoCore Status Overlay**  
Runtime-oriented overlay concept for tracking current task, broader project, completed stages, next required steps, files in scope, and system path.

## Metadata Terms Present in Source
**molt_type**  
Declared structural role of a block, here using values such as `Primary`, `Instruction`, `Philosophy`, and `Subject`.

**trigger**  
Optional behavior object describing when and how a block should activate or lead to another block.

**ledger**  
Provenance and lineage metadata retained as part of structured block understanding and export.

**export_config**  
Metadata describing how a block or its content should be exported or serialized.

## Definitional Candidates
Metadata stays in exports even if UI display varies.  
Blocks should be inspectable at both normal meaning level and UMG/MOLT meaning level.  
Block introspection is self-description, not sentience.  
Hackathon scope is intentionally non-Web3 for the current build.

# BATCH-200 — Blocks / MOLT Extract

## Scope
This extract captures role semantics and modular block design language preserved in the batch.

## Explicit Roles
- Primary Block
- Merge Block
- Blueprint Block

## Role Readings
### Primary
Represents user intent or the core prompt.

### Merge
Represents context, auxiliary data, retrieved information, or tool results that should be fused into reasoning.

### Blueprint
Represents style, format, tone, or response philosophy.

## Composition Pressure
- Modular block implementations may benefit from a shared interface or base class.
- Blocks are treated as configurable, enable/disable-able logic units.
- Visual composition is described as user selection/configuration of blocks into a reasoning surface.

## Stability Notes
This batch uses a simplified public-facing Primary / Merge / Blueprint framing rather than deeper canonical MOLT layering.

## Project Relevance
Useful for:
- public explanation of block roles
- implementation-facing block interface planning
- Merge-as-context/capability support discussions

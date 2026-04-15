# BATCH-174 — Definitions Extract

## MOLTType
The top-level category key used to organize the builder library in this batch.

## BlockMeta
A starter metadata shape for a selectable block, using:
- `id`
- `label`
- `description`

## BlockShelf
A grouped record keyed by MOLT type and storing arrays of `BlockMeta`.

## blockLibrary
The definition-layer object holding categorized block inventories.

## BlockPalette
The UI surface that displays categorized blocks and acts as the drag source.

## Canvas
The drop target and temporary runtime surface for placed blocks.

## Primary
Used here as the category for core layout / structural website elements.

## Subject
Used here as the category for content/domain page units.

## Instruction
Used here as the category for behavior / logic / rendering-related units.

## Philosophy
Used here as the category for stylistic or design-language overlays.

## Directive
Used here as the category for strategic, optimization, policy, or operational behaviors.

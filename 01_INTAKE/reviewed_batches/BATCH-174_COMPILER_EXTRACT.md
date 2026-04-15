# BATCH-174 — Compiler / Runtime Extract

## Runtime Path in This Batch
1. User drags a block from the palette
2. Canvas accepts the dropped block
3. Block metadata is appended into local placed state
4. Canvas renders a placeholder element for the dropped item

## Concrete Runtime Pieces
- `react-dnd`
- `HTML5Backend`
- drag source: `BlockPalette`
- drop target: `Canvas`

## Current Limits
- no serialization/export
- no nested composition
- no prop editor
- no real semantic renderer dispatch by block id
- no persistence layer
- no inspector panel

## Candidate Runtime Next Step
Replace placeholder dropped cards with real renderers keyed by block id while keeping the definition layer independent from UI logic.

## Workflow Constraint
Bolt terminal behavior appears inconsistent for heredoc/redirection flows. Future runtime/build workflows should support editor-safe or terminal-safe update methods.

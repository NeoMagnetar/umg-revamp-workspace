# BATCH-108 — NeoStructure Extract

## Core structural model
This batch describes a **rooted graph-stack hybrid** rather than a freeform graph.

## Main structure rules
1. Primary is the root / top entry node.
2. Nothing may be placed above Primary.
3. Vertical placement creates stack depth.
4. Horizontal placement creates overlay / sibling / merge candidate behavior.
5. Blank-space drops may start a new stack group.
6. Stack order and grouping must survive save/load.

## Visual / logical mapping
- **Vertical axis** → priority, sequence, deeper logic
- **Horizontal axis** → overlay, modifier, merge opportunity
- **Root emphasis** → Primary as brainstem / entrypoint

## Suggested visual reinforcements
- Root framing for Primary
- Stack lanes / column guides
- Semi-fixed or protected root behavior
- Explicit merge affordances
- Clear distinction between stack and overlay edges

## Builder surface model
- Left: block library / categories
- Center: graph canvas
- Right: JSON editor / block inspector
- Bottom: future terminal / command panel

## Structural risk
Using a generic graph editor without rooted constraints risks turning UMG into an unconstrained flowchart and losing semantic hierarchy.

## Disposition
Strong candidate evidence for builder neostructure behavior; still provisional until merge UX, panel arrangement, and save/export state model are stabilized.

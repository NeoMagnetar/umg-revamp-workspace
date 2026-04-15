# BATCH-108 — Definitions Extract

## Core terms

### UMG Builder
A builder interface for composing structured logic, plans, and AI cognition using UMG blocks, intended to behave more like a thought IDE / mind IDE than a generic drag-and-drop canvas.

### Primary
Mandatory root block. Treated as the starting point of a stack. Nothing should be placed above it.

### Subject
Domain or scope context block.

### Instruction
Rule / process / constraint block.

### Philosophy
Tone, ethics, worldview, or evaluative lens block.

### Blueprint
Layout / format / rendering logic block, distinct from behavior and from executable code payload.

### Directive
Strategic steering or emphasis block.

### Trigger
Execution condition / activation block. Present as a role and distinct from graph positioning or generic code payload.

### Deployment
Builder-facing role described in this packet as environment/version target. Status remains unresolved as a valid long-term MOLT role.

### Off
Inactive or disabled block state/role.

## Architecture language

### Vertical placement
Represents stack depth / hierarchy / priority.

### Horizontal placement
Represents overlay, sibling modification, or merge candidate behavior.

### Stack priority
Metadata-driven ordering concept for vertical placement and serialization / restoration.

### Stack group
Grouping concept used to preserve related blocks within one stack/root context.

### Merge engine
Proposed runtime component responsible for determining whether two blocks can merge and how merged state is formed.

### Snap logic
Runtime decision layer that determines whether a drag/drop action should create:
- vertical stack placement
- horizontal overlay / merge attempt
- rejected placement

### Thought IDE / Mind IDE
Proposed experiential framing for the builder: code-space-like, structured, inspectable, and logic-first.

## Runtime / file language

### `GraphCanvas.tsx`
Main graph canvas surface for rendering and manipulating block nodes.

### `flowUtils.ts`
Utility layer for converting block data into node/edge representations and restoring ordered state.

### `snapLogic.ts`
Utility layer for distinguishing vertical stack snaps from horizontal merges/overlays.

### `mergeEngine.ts`
Utility layer for merge validation and merge execution.

### JSON editor panel
First-class editing surface where a selected block remains editable as JSON / code-like data rather than only via visual controls.

## Open definition candidates
- Whether `Deployment` is a durable MOLT role.
- Whether Primary should be fully locked in place or only structurally protected.
- Exact meaning of merge result persistence and undo behavior.

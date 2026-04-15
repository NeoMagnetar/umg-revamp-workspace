# BATCH-169 — NeoStructure Extract

## Why this extract exists
This source defines a builder-facing structure for how blocks, stacks, sleeves, sections, panels, and repo layout should relate to one another. fileciteturn19file0

## Structural Layers Preserved
### Block layer
Self-describing JSON units with role, merge, snap, runtime, provenance, and optional modules.

### Stack / section layer
Blocks arranged vertically/horizontally with snap-to-grid or snap-together behavior, plus grouping into stacks and sections.

### Sleeve layer
Persona/runtime assemblies loaded from sleeve JSON and reflected into active runtime state.

### Builder surface
- left-side visual block UI/canvas
- right-side raw JSON/code representation
- drag/drop manual stacking
- automatic stacking / auto-populate options
- wireframe skeleton mode
- collapsible sleeves, stacks, and sections

### Repo / filesystem layer
- `blocks/` as canonical root
- runtime memory files under `memory/`
- repair/registry/loader logic under source modules and maintenance scripts. fileciteturn19file0

## Structural Risk Preserved
Folder cleanup and canonicalization were still underway during the source conversation, so keep structure as evidence rather than final canon.

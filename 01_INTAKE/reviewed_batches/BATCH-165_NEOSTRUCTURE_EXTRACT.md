# BATCH-165 NeoStructure Extract

## Structural Signal
The batch describes a layered builder architecture with clear separation between content/model surfaces and render/runtime surfaces.

## Implied Structural Layers
### Data / Model Layer
- manifests
- per-block JSON files
- optional aggregated `blocks.json`

### Active Composition Layer
- stack loading
- canvas block state
- selected plan state
- block library inventory vs active workspace

### Rendering / Interface Layer
- block library pane
- canvas/editor pane
- graph/flow renderer
- properties/inspector panes

### Packaging / Migration Layer
- Bolt export ZIP
- GitHub repo population/replacement
- unified diff / overwrite scripts

## Structural Insight
The builder is not one flat app surface. It is a modular system where data, active state, rendering, and packaging all have distinct responsibilities. This is strong evidence for UMG-style structural separation in the builder ecosystem.

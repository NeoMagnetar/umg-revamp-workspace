# BATCH-165 Definitions Extract

## UMG Builder
The application surface used to load, edit, display, and organize UMG blocks and stacks.

## Manifest-Driven Loading
A selected plan loads through a manifest that lists block IDs, which are then loaded individually and rendered into canvas/graph state.

## Block Integrity
The requirement that block data be valid, uniquely identified, and internally consistent before rendering:
- unique IDs
- valid JSON
- valid edges/references

## Per-Block JSON
A storage pattern where individual block definitions live as separate files such as `.block.json`.

## Aggregated `blocks.json`
A possible alternate or supplemental storage/index surface that may summarize or collect block definitions for downstream use.

## Stack Loading
Runtime behavior that reads stack-associated block IDs and populates active canvas/editor state.

## Graph Rendering
The UI/runtime surface that visualizes nodes/edges representing builder relationships and must remain distinct from storage/data concerns.

## ErrorBoundary
A rendering guard that surfaces UI/runtime failures visibly instead of letting the graph disappear silently.

## Hard Replacement
A repo migration/update mode where the target codebase is fully replaced by the intended exported artifact rather than incrementally merged.

## Unified Diff Patch
A patch artifact that describes exact file changes for local or repo application.

## Zero-Height Container Failure
A rendering failure where the graph surface exists but cannot display because its container has no effective height.

## Duplicate Folder Contamination
A repo state issue caused by extracted nested folders or overlapping copies, leading to path ambiguity and unstable runtime behavior.

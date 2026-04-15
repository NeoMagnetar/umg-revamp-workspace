# BATCH-082 — Compiler / Runtime Extract

## Scope
This extract captures builder/runtime-facing logic implied by the batch.

## Source-Backed Points
- Builder semantics include snapping, stacking, merge-any-block behavior, and skeleton mode.
- Hierarchy is expected to store parent/child and possibly peer-level relationships.
- Some blocks may remain attached below a merged core rather than being flattened into it.
- Builder state is expected to carry metadata such as role/type, labels, merged summary, relationship state, and possibly scope/apply-to targeting.
- Future searchable preset/database behavior is implied.

## Runtime / Compiler Pressure
The batch implies a front-end graph or tree model with at least these possible surfaces:
- typed node
- parent-child relation
- peer relation
- merge relation
- merged summary
- scoped attachment
- skeleton representation

## Open Implementation Pressure
- How does snapped hierarchy serialize?
- How are lower-hierarchy attachments represented in runtime?
- Does skeleton mode produce an export structure or only a view?
- How do merge-any-block semantics map back to earlier token-weight / priority execution logic?
- Should role naming at the builder layer be normalized before export or preserved as user-facing labels?

## Conservative Intake Reading
Useful for:
- builder object-model design
- graph serialization questions
- runtime authoring semantics
- export-format planning

Not enough to:
- finalize compiler law
- finalize merge precedence
- finalize numeric priority execution

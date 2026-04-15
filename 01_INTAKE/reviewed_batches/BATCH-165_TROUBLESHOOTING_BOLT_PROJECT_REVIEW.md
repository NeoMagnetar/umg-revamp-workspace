# BATCH-165 Troubleshooting Bolt project — Review

## Source Snapshot
This batch records diagnosis and repair planning for the UMG Builder application hosted in Bolt and mirrored to GitHub. The main reported failures were empty or messy builder rendering, blocks not loading, and graph/flow visualization failure. The conversation progressed from debugging hypotheses into implementation guidance, repo replacement strategy, export workflows, and later UI polish recommendations.

## Chat-Level Summary
The strongest source signal is that the UMG Builder is block-centric, manifest-driven, stack-aware, and graph-rendered. The chat repeatedly separated data/model concerns from rendering concerns:
- manifests and per-block JSON define content
- loaders populate block/state data
- graph/canvas/UI panes render that data
- repo/export workflows package the application surface for maintenance and release

The chat also emphasized that silent failures are unacceptable. Duplicate IDs, invalid edges, failed fetches, bad content-types, and zero-height containers should surface visible errors instead of degrading invisibly.

## UMG-Relevant Extraction
- Blocks are the primary working unit.
- A selected plan loads through a manifest, which references block IDs, which are then loaded individually.
- Stack handling is implied through `handleLoadStack` and canvas population.
- The builder expects a graph view that represents UMG relationships such as stack, snap, merge, and philosophy.
- Builder maturity depends on explicit validation, not silent fallback.
- The builder is a runtime/editor surface for assembling and inspecting UMG structures.

## Independent Review
This is strong implementation evidence for the current builder/runtime surface. It is not a semantic canon source, but it is materially relevant to:
- block storage layout
- manifest-to-block load pipeline
- stack/canvas distinction
- graph/render failure classes
- validation and maintenance workflows

The batch contains both confirmed patterns and provisional diagnosis. The confirmed patterns are the block-centric builder model, manifest-driven loading flow, rendering/data separation, and the push toward explicit validation. The more provisional material includes the exact source-of-truth file layout (`blocks.json` vs per-block `.block.json`) and some inferred paths used during debugging.

## Roadmap Mapping
- **Phase 2 — Compiler Impact:** validation, deterministic layout, integrity checks, loader hardening
- **Phase 3 — Documentation Impact:** document block storage, manifest loading, error classes, export/replacement workflow
- **Phase 5 — PRD and Staging:** builder stability criteria, repo replacement strategy, graph/navigation requirements
- **Phase 6 — GitHub Execution:** patch generation, repo overwrite strategy, validation scripts, CI checks

## Disposition
**ACCEPT_AS_EVIDENCE**

Reason:
- strong implementation signal for UMG Builder runtime surfaces
- direct relevance to builder reliability, graph rendering, and maintenance workflow
- clear boundary between confirmed architecture and provisional diagnosis can be preserved without canon promotion

## Notes
This batch should remain evidence-first. It contributes builder/runtime facts and candidate work items, but it does not settle builder canon or final storage law.

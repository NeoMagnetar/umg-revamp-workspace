# BATCH-135 — Compiler Extract

## Scope
Compiler-facing implementation implications extracted from the source.

## High-Value Compiler Claims
1. Blocks may need explicit manifests, typed input contracts, output contracts, validators, trace emission, and artifact trees.
2. Schema blocks and process blocks are first-class artifact types, not just prose sections.
3. Adapters should translate shape while blocks enforce meaning.
4. Compiler/intake behavior should remain deterministic and non-analytical during capture when the block’s role is acquisition rather than interpretation.
5. Process-authoritative blocks should expose phase gates, required artifacts, and failure modes.
6. The compiler or surrounding system should preserve read-only, no-write, no-covert-access, and evidence-linked constraints as structural boundaries.
7. Recursive decomposition should remain architecturally legal without forcing every artifact class to share the same internal tree.
8. Rendering fidelity should be treated as a renderer-layer problem, not as a semantic-block problem.

## Likely Compiler Audit Targets
Manifest and contract shape for block registration.
Schema/process block classification rules.
Artifact-tree-bearing block support.
Adapter versus semantic enforcement boundaries.
Trace logging expectations for process-authoritative blocks.
Separation of semantic render structure from renderer typography.

## Risk Surface
Any system that collapses renderer typography into block semantics would conflict with this batch.
Any template system that injects unrelated modules into blocks would conflict with the block-native section doctrine.
Any adapter layer that rewrites block meaning instead of only translating shape would conflict with the extracted architecture.

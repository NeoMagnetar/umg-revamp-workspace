# BATCH-054 — Compiler Extract

## Scope
Compiler/runtime-adjacent implications from the block-generation workflow batch.

## Confirmed Signals
- The source strongly prefers a one-pass importer/generator over manual micro-batching.
- The intended workflow reads from a master list and emits properly named files into repo directories.
- The generator should preserve canonical names rather than using generic placeholders.
- The workflow is expected to support later Poecore interpretation and assembly logic.

## Candidate Compiler Surfaces
### Import Surface
- read plain source list
- normalize labels
- assign IDs
- assign or preserve MOLT type
- write to correct repo path

### Validation Surface
- ensure minimum valid block fields exist
- audit missing names/descriptions/types
- detect numbering collisions or resets
- detect placeholder blocks that violate naming fidelity

### Normalization Surface
- distinguish global numbering from category-local numbering
- separate required fields from optional fields
- preserve provenance ledger entries

### Runtime Preparation Surface
- expose snap/merge-compatible metadata
- preserve stackable/mergeable fields without pretending runtime is finalized
- leave room for Poecore or later orchestrators to consume the output contract

## Risks
- Over-complete schema may block initial import if required too early.
- Placeholder-first imports may poison later canonicalization.
- Numbering policy drift can break references and audits.
- Source-of-truth ambiguity can create divergent block inventories.

## Recommended Follow-On
Create a compiler-spec decision that separates:
1. required import fields,
2. optional enrichment fields,
3. post-import derivable fields,
4. audit rules for naming fidelity and numbering continuity.

# BATCH-098_DEFINITIONS

## Scope Note
These definitions are extracted from a derived source summary. They are evidence candidates, not canon.

## Terminology Extract

### UMG Block Metadata Policy (v1.0)
- Governance structure defining the required metadata fields and behavior expectations for all UMG blocks.
- Presented as ensuring clarity, traceability, and interoperability across different use and export contexts.

### Block library
- Growing inventory of reusable UMG blocks accumulated section by section rather than regenerated from scratch.

### Injection-ready block
- Block prepared for reuse anywhere in the app or workflow, including load/fork behavior and export-retained metadata.

### Skeleton tree / branched organization
- Hierarchical organization model for grouping blocks by domain, subdomain, and function.

### Category path
- Structured storage path used to organize block inventory by business domain and functional class.

## Role Language

### Primary
- MOLT role assigned in-source to business plan type blocks.
- Used for top-level functional or defining plan classes.

### Instruction
- MOLT role assigned in-source to business plan subtype / format blocks.
- Used for procedural, formatting, or applied execution-oriented content classes.

### Subject
- Proposed in-source for future report / section blocks.
- Not yet executed in the source batch; remains a forward-looking mapping signal.

### Philosophy
- Included in the metadata policy as an available MOLT role, but not the main focus of the generated examples in this batch.

## Architecture Language

### block_id
- Unique identifier field for a block.
- The summary notes tension between slug-style IDs in examples and the policy allowance for uuid-or-hash conventions.

### editable_fields
- Declared mutable block components intended for controlled adaptation or reuse.

### canto_overlay
- Metadata field associated with overlay or organizational layering.
- Exact semantic boundary between this field and the end-of-message presentation overlay remains unresolved.

### ledger
- Provenance and lineage-tracking field associated with remix/fork history and traceability.

### trigger
- Explicit behavioral metadata field attached to block reuse or fork events.

### export_config
- Field governing export behavior and retained metadata expectations across destinations.

## Runtime / Compiler Language

### on_use trigger
- Runtime/event hook invoked when a block is loaded or used.

### on_fork trigger
- Runtime/event hook invoked when a block is remixed or forked, often tied to logging or edit history behavior.

### additive ingestion
- Section-by-section expansion model where new block sets are added to the library without rebuilding the whole inventory.

### export-retained attribution
- Governance rule in which attribution-related metadata remains in export even when UI display is optional or suppressed.

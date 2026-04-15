# BATCH-098_BLOCKS_MOLT_EXTRACT

## Scope
MOLT / metadata / block-schema signals extracted from BATCH-098.

## Core MOLT Mapping Signal
The source gives one of the clearest domain-specific mappings of content classes into MOLT roles:
- plan types → Primary
- subtypes / formats → Instruction
- future report / section blocks → Subject (announced, not executed)

This is important because it applies MOLT by block function rather than by abstract theory alone.

## Standard Metadata Envelope
The source reports a fixed block envelope including:
- block_id
- label
- category
- description
- editable_fields
- molt_type
- tags
- canto_overlay
- ledger
- trigger
- export_config

This strongly pressures documentation toward a mandatory-versus-optional field distinction.

## Block Behavior Signal
Blocks are described as:
- injection-ready
- fork-ready
- metadata-governed
- organized by category path
- exportable without repeated repackaging

The batch treats editable fields and triggers as part of core block composition, not decorative extras.

## Structural Tensions
- example values for trigger, overlay, and export_config may be implementation defaults rather than settled canon
- the exact semantics of `canto_overlay` remain unresolved
- the relation between metadata overlay and end-of-message organizational overlay is not stabilized
- block ID rules are not finalized despite policy allowance for multiple ID styles

## High-Value Documentation Targets
- formalize the block metadata policy as a schema candidate
- clarify how MOLT role assignment should work for domain-content blocks
- distinguish governance fields from runtime-execution fields
- define stable ID conventions
- clarify overlay semantics across metadata and presentation surfaces

# BATCH-080_BLOCKS_MOLT_EXTRACT

## Scope
Role and block-taxonomy material explicitly supported by the source.

## Source-Backed Role Behavior
- **Primary**
  - Activates system mode.
  - Example: `RAG.ENABLED.MODULE`
- **Subject**
  - Defines retrieval domain or context.
  - Example: knowledge graph / external source domain
- **Philosophy**
  - Sets behavioral hierarchy.
  - Example: `TRUTH > STYLE`
- **Instruction**
  - Defines execution pipeline.
  - Example: `RETRIEVE > INJECT > RENDER`
- **Merge**
  - Implicitly extended from static support content to dynamic retrieval carrier

## Candidate Taxonomy Pressure
This batch suggests that Merge may need two distinguishable forms:
- **Static Merge**
  - fixed support text/content
- **Dynamic Merge**
  - retrieval-backed support content injected at runtime

## Candidate Field Pressure
The source explicitly or implicitly supports:
- type
- cantocore / role string
- content or retrieval target
- execution role
- runtime priority / truth hierarchy

## Notes
- The batch does **not** finalize RAG as a canonical NeoBlock type.
- The batch does **not** resolve whether RAG belongs inside normal role taxonomy or adjacent to it as a subsystem.

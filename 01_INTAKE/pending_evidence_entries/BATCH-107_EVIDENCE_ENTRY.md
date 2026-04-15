# BATCH-107 — Evidence Entry

- **Batch ID:** BATCH-107
- **Title:** Block Builder Schema and Recovery
- **Source type:** Derived extraction / handoff note
- **Disposition:** ACCEPT_AS_EVIDENCE
- **Review status:** REVIEWED
- **Primary domain:** block builder schema, validation, and recovery workflow
- **Roadmap tags:**
  - PHASE_1_CORE_ALIGNMENT
  - PHASE_2_COMPILER_IMPACT
  - PHASE_3_DOCUMENTATION_IMPACT
  - PHASE_4_SKILL_ALIGNMENT
  - PHASE_5_PRD_AND_STAGING

## Signal Summary
- Clarifies builder-facing distinction between browsing taxonomy and MOLT runtime role.
- Stabilizes a working MOLT role set including Trigger and CodeBlock while treating Deployment as problematic legacy.
- Produces strong evidence for strict schema validation, legacy normalization, and CI enforcement.
- Surfaces unresolved tensions around `domain`, final folder layout, manifest flow, and schema strictness.

## Evidence Value
- Strong for schema/documentation/compiler impact.
- Medium-to-high contradiction load.
- High duplicate pressure with prior schema, metadata, and reorg batches.

## Next Decision Target
- Single canonical block-builder data contract for schema, role taxonomy, and routing behavior.

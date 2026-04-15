# BATCH-201 — Project Impact

- **primary domain:** repo_structure_and_builder_runtime
- **roadmap phases touched:**
  - PHASE_1_CORE_ALIGNMENT
  - PHASE_2_COMPILER_IMPACT
  - PHASE_3_DOCUMENTATION_IMPACT
  - PHASE_4_SKILL_ALIGNMENT
  - PHASE_5_PRD_AND_STAGING
- **contradiction watch:** HIGH
- **duplicate pressure:** HIGH
- **likely downstream targets:**
  - schema reference cleanup
  - manifest and validator docs
  - sleeve/stack separation docs
  - Poe builder integration planning
  - canonical block tree enforcement
- **next decision target:** `Deployment` and `Merge` status across schema, runtime, and builder logic

## Impact Notes
This batch matters because it reduces structural ambiguity in the implementation repo:
- one file per block
- generated manifests from canonical blocks
- stacks/sleeves separated from schema/config layers
- runtime scripts aligned to canonical locations

It also creates pressure to reconcile docs with actual runtime choices, especially where the schema reference and runtime cleanup disagree.

## Intake Disposition Rationale
The batch remains evidence because the migration direction is strong, but semantic cleanup and final integration architecture are still in motion.

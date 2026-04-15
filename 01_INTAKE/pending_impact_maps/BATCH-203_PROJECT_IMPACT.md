# BATCH-203 — Project Impact

- **primary domain:** canon_storage_and_runtime_separation
- **roadmap phases touched:**
  - PHASE_1_CORE_ALIGNMENT
  - PHASE_2_COMPILER_IMPACT
  - PHASE_3_DOCUMENTATION_IMPACT
  - PHASE_4_SKILL_ALIGNMENT
  - PHASE_5_PRD_AND_STAGING
- **contradiction watch:** HIGH
- **duplicate pressure:** MEDIUM
- **likely downstream targets:**
  - schema definition
  - naming conventions
  - loader contract
  - file registry layout
  - canonization workflow docs
- **next decision target:** lock one-object-per-file schema and loader semantics or continue refinement

## Impact Notes
This batch matters because it moves UMG out of the model and into a governed file system. That creates a durable foundation for:
- persistent canon
- agent-usable loading
- versioned object identity
- privacy-preserving selective projection
- clean separation between source, mapping, and runtime

It also creates pressure to standardize object format, dependency references, and loading rules sooner rather than later.

## Intake Disposition Rationale
The batch remains evidence because the architectural direction is strong, but the exact schema and loader protocol are still open.

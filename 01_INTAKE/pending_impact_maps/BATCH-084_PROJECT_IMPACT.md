# BATCH-084 — Project Impact

- **primary domain:** runtime_deployment_architecture
- **roadmap phases touched:**
  - PHASE_1_CORE_ALIGNMENT
  - PHASE_2_COMPILER_IMPACT
  - PHASE_3_DOCUMENTATION_IMPACT
  - PHASE_4_SKILL_ALIGNMENT
  - PHASE_5_PRD_AND_STAGING
- **contradiction watch:** HIGH
- **duplicate pressure:** MEDIUM
- **likely downstream targets:**
  - compiler task spec
  - runtime flow document
  - backend orchestration design
  - JSON config normalization
  - deployment staging plan
- **next decision target:** minimal executable runtime spine vs expansive platform scope

## Impact Notes
This batch materially advances UMG from framework language into system architecture. It pressures the project to make choices about:
- which runtime components are core
- which config surfaces are canonical
- how model routing and fallback should actually behave
- whether privacy/alignment/HUD are first-class runtime layers or later shells
- what the v1 release boundary really is

It is especially useful because it defines not only concepts, but also named functions, endpoints, config files, and runtime sequences.

## Intake Disposition Rationale
The batch remains evidence because it mixes:
- concrete function/route/config ideas
- aspirational platform scope
- scaffold-level code direction
- unresolved frontend/backend wiring gaps

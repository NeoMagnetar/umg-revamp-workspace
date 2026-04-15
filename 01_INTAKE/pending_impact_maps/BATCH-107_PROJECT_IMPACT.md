# BATCH-107 — Project Impact

## Primary Domain
block builder schema, validation, and recovery workflow

## Roadmap Phases Touched
- PHASE_1_CORE_ALIGNMENT
- PHASE_2_COMPILER_IMPACT
- PHASE_3_DOCUMENTATION_IMPACT
- PHASE_4_SKILL_ALIGNMENT
- PHASE_5_PRD_AND_STAGING

## Contradiction Watch
HIGH

## Duplicate Pressure
YES

## Likely Downstream Targets
- 03_CORE_ALIGNMENT/canonical_decisions
- 04_COMPILER/audit and task-spec work
- 05_DOCUMENTATION/core_definitions
- 06_SKILLS/skill alignment and builder-adjacent skills
- 07_PRD_AND_STAGING/final PRD package

## Project Impact Summary
This batch materially affects the control project because it converts abstract UMG semantics into concrete builder data-layer requirements. It pressures the project to explicitly settle role taxonomy, schema field legality, migration rules, and metadata-driven routing before any serious Block Builder restoration or UI recovery can be considered stable.

## Next Decision Target
canonical builder data contract:
- folder taxonomy vs schema field taxonomy
- `Deployment` status
- strict migration vs permissive normalization

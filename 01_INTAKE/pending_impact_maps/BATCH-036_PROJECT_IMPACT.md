# BATCH-036 — Project Impact Map

## Primary Domain
Runtime architecture framing

## Roadmap Phases Touched
- PHASE_1_CORE_ALIGNMENT
- PHASE_2_COMPILER_IMPACT
- PHASE_3_DOCUMENTATION_IMPACT
- PHASE_4_SKILL_ALIGNMENT
- PHASE_5_PRD_AND_STAGING

## Contradiction Watch
MEDIUM

## Duplicate Pressure
HIGH

## Likely Downstream Targets
- `05_DOCUMENTATION/core_definitions`
- `05_DOCUMENTATION/sleeves`
- `05_DOCUMENTATION/neoblocks_and_neostacks`
- `04_COMPILER`
- `07_PRD_AND_STAGING`

## Project Impact
This batch strengthens the project-level framing that UMG should be understood as a control architecture layered over inference, not as a monolithic prompt artifact. It also sharpens the implementation gap: governance, state, validation, and ordered execution remain largely declarative until they move into runtime/controller infrastructure.

## Why It Matters
- clarifies long-range identity of the project
- supports documentation language for runtime evolution
- provides a staged transition model from prompt-declared architecture to executable controller
- supports PRD narrative for minimal-runtime-first development

## Next Decision Target
Decide the minimum runtime/controller contract required for the project to claim movement from declarative UMG toward executable UMG.

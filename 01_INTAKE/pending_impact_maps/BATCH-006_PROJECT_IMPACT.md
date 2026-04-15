# BATCH-006 — Project Impact Map
## Primary Domain
compiler-runtime-alignment

## Roadmap Phases Touched
- PHASE_1_CORE_ALIGNMENT
- PHASE_2_COMPILER_IMPACT
- PHASE_3_DOCUMENTATION_IMPACT
- PHASE_4_SKILL_ALIGNMENT
- PHASE_5_PRD_AND_STAGING

## Contradiction Watch
MEDIUM

Primary tension:
- UMG conceptually treats MOLT as an authority model
- the current compiler mostly performs layout/assembly and indexing rather than full authority resolution

Secondary tension:
- “active” runtime output can appear stronger than the compiler’s actual conditional resolution behavior
- several proposed metadata and runtime-path features are implementation candidates, not yet finalized contract

## Duplicate Pressure
HIGH

Likely overlap zones:
- governance anchoring
- MODE vs BP_MODE separation
- block / stack / sleeve / NeoStack definitions
- bounded-agency runtime loop material
- compiler modernization and next-version pathing
- project-mode repo / portable brain cartridge workflow

## Likely Downstream Targets
- 04_COMPILER/intake_extracts
- 05_DOCUMENTATION/core_definitions
- 05_DOCUMENTATION/blocks_and_molt
- 05_DOCUMENTATION/neoblocks_and_neostacks
- 05_DOCUMENTATION/sleeves
- 07_PRD_AND_STAGING

## Next Decision Target
Resolve whether Authority Resolution, resolvedStates, and runtime tag/signal evaluation become:
- first-class compiler contract surfaces
- adjunct runtime-only logic
- or a staged hybrid split across compiler and runtime

# BATCH-109 — Project Impact

## Primary Domain
core ontology, terminology correction, and compiler/runtime boundary clarification

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
- `03_CORE_ALIGNMENT/canonical_decisions`
- `05_DOCUMENTATION/core_definitions`
- glossary/spec sections covering CSL, UMG, CIR, Compiler, RuntimeSpec, Trace, PCL
- compiler/task specs that currently use CSL compilation language
- skill/runtime docs that blur executor behavior with cognition ownership

## Impact Summary
This batch creates direct pressure to clean up a foundational category error. If left unresolved, CSL-as-language or CSL-compiles-into-CIR language will pollute specs, compiler descriptions, and public-facing materials. The strongest project impact is definitional and architectural rather than implementation-specific.

## Next Decision Target
canonical terminology correction for CSL, UMG, CIR, RuntimeSpec, Trace, and compiler wording

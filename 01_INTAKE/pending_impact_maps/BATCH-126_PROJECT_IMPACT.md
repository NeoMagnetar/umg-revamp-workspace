# BATCH-126 — Project Impact

## Primary Domain
Compiler-facing structural semantics and staging guidance

## Roadmap Phases Touched
PHASE_1_CORE_ALIGNMENT
PHASE_2_COMPILER_IMPACT
PHASE_3_DOCUMENTATION_IMPACT
PHASE_4_SKILL_ALIGNMENT
PHASE_5_PRD_AND_STAGING
PHASE_6_GITHUB_EXECUTION

## Contradiction Watch
MEDIUM

Reason:
This batch is internally coherent, but it may conflict with other evidence on whether MOLT is semantic ordering only versus a stronger authority system, and on whether governance is optional support or the sole override mechanism.

## Duplicate Pressure
MEDIUM to HIGH

Reason:
The batch overlaps strongly with prior evidence on MOLT order, bundle vs merge, NeoBlock and NeoStack structure, compiler outputs, trace requirements, and repo split recommendations.
Downstream handling should merge concepts rather than repeat them.

## Likely Downstream Targets
03_CORE_ALIGNMENT/candidate_fragments
03_CORE_ALIGNMENT/canonical_decisions/CANONICAL_DECISIONS_LOG.md
04_COMPILER/audit/COMPILER_AUDIT_LOG.md
05_DOCUMENTATION/release_docs/DOC_UPDATE_LOG.md
06_SKILLS/skill_alignment_matrix/SKILL_ALIGNMENT_MATRIX.md
07_PRD_AND_STAGING/final_prd/PRD_UMG_REVAMP_TEMPLATE.md

## Immediate Impact Notes
The rejection of `stack_rank` and replacement with `priority_group` is the most direct compiler/design consequence in the batch.
The source also sharpens the structural ladder from Block to Sleeve and insists that UI behavior must map into explicit compiler metadata rather than hidden semantics.
It is useful both as a semantic clarification source and as staging guidance for headless compiler vs public Studio separation.

## Next Decision Target
priority_group adoption and MOLT/governance boundary review

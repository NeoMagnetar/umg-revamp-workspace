# BATCH-128 — Project Impact

## Primary Domain
Compiler and Studio boundary clarification with release-path implications

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
The batch is internally coherent, but it sits near live drift zones:
priority wording,
UI surfacing,
bundle/merge versus NeoBlock compression,
and runtime targeting between legacy shell and real Studio app.
These may conflict with older summaries or provisional implementation assumptions.

## Duplicate Pressure
MEDIUM to HIGH

Reason:
This batch overlaps with prior compiler glossary, GitHub scaffold, Replit recovery, and compiler release batches.
The correct downstream move is concept-merge rather than repeated restatement.

## Likely Downstream Targets
03_CORE_ALIGNMENT/canonical_decisions/CANONICAL_DECISIONS_LOG.md
04_COMPILER/audit/COMPILER_AUDIT_LOG.md
05_DOCUMENTATION/release_docs/DOC_UPDATE_LOG.md
06_SKILLS/skill_alignment_matrix/SKILL_ALIGNMENT_MATRIX.md
07_PRD_AND_STAGING/final_prd/PRD_UMG_REVAMP_TEMPLATE.md

## Immediate Impact Notes
The batch materially reduces semantic confusion by separating:
authoring truth,
compiler truth,
and UI/editor state.
It also gives a strong documentation target: subset bundle/merge inside a stack must not be confused with compressing a whole stack into a NeoBlock.
The release signal is also important: the compiler can stand as publishable infrastructure even if Studio remains unfinished.

## Next Decision Target
bundle_merge_vs_neoblock_compression_boundary

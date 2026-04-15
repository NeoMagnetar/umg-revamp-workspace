# BATCH-159 — Compiler Extract

## Compiler / runtime-relevant findings
- Instruction remains active while conditions are stable.
- Trigger changes active execution state when assumptions fail.
- Directive may assert new control after Trigger.
- Merge refines the active strategy without replacing Primary.
- Off remains stored but inactive until relevant.

## Candidate runtime implications
### Trigger
- Model as a condition evaluator that can change active state.

### Directive
- Evaluate whether runtime needs two Directive modes:
  1. reactive override mode
  2. standing doctrine mode

### Merge
- Treat as refinement input to active strategy rather than mission replacement.

### Off
- Treat as stored-but-inactive logic with explicit reactivation conditions.

## Audit note
This source is analogy-driven, so it should inform runtime interpretation but not directly define parser or schema rules without later normalization.

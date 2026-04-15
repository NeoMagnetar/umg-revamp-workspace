# BATCH-121_COMPILER_EXTRACT

## Compiler / Validation-Relevant Signal
- Enforce one-question-per-block validation.
- Enforce single fixed-role membership for every block.
- Enforce non-mutation of block meaning once instantiated.
- Apply governance exclusion before trigger or priority participation.
- Produce trace output listing:
  - what participated
  - what was excluded
  - why selection occurred
- Preserve deterministic outcomes under identical inputs.

## Candidate Compiler Tasks
- Validate fixed block-role membership.
- Reject inferred intent.
- Reject participation by governance-excluded elements.
- Keep triggers as eligibility checks only.
- Keep priority scoped to single conflict sites only.
- Require trace for validity.
- Fail invalid outputs when no explainable trace exists.

## Risks
- Merge is underdefined in this batch.
- OFF is asserted but not represented procedurally here.
- Blueprint and runtime sequencing remain thin.
- Strong principle language may outrun current mechanism detail if adopted without companion specs.

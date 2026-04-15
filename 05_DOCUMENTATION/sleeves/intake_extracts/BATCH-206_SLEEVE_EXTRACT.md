# BATCH-206 — Sleeve Extract

## Scope
This extract captures sleeve identity, resleeving, and mutation control in the runtime design.

## Sleeve Reading
A sleeve is the active runtime configuration for a task. It governs:
- which stacks load
- permissions
- budgets
- philosophy
- cost ceiling
- mutation permissions

## Sleeve Fields Mentioned
- sleeve_id
- description
- stacks
- permissions
- budgets
- author
- created_at

## Example Sleeve IDs
- SLV.POE_UMG.MAIN.v1
- SLV.CODING.AGGRESSIVE.v1

## Resleeving Semantics
- only one sleeve is active per task context
- agents may request sleeve switches
- orchestrator validates
- optional human approval may be required
- mutation always produces version increments
- critical sleeves may be locked against agent mutation

## Drift / Control
Sleeve drift detection tracks:
- block churn
- stack instability
- permission creep

## Project Relevance
Useful for:
- sleeve schema docs
- resleeving approval flow
- lock/mutation policy
- cost/budget posture by sleeve

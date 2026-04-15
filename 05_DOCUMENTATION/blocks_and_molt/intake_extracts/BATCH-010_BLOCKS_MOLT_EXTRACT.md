# BATCH-010 Blocks / MOLT Extract

## MOLT-Relevant Use
The batch treats MOLT as a runtime parsing scaffold for governance audits and continuity enforcement, not only for normal task/content work.

## Trigger Signals Observed
- termination request
- override request
- reset/new-session request
- bypass-prompt request
- minimal-response request
- reentry/audit request

## Functional Block Candidates
- `NB.GOV.CONTINUITY.PERSISTENCE.v1`
- `NB.INSTRUCTION.CONTROL_PAYLOAD.CLASSIFIER.v1`
- `NB.INSTRUCTION.WRAPPER.PERSISTENCE.v1`
- `NB.AUDIT.PRESENTATION.DRIFT.v1`
- `NB.REANCHOR.CONTINUITY.RESTORE.v1`

## Suggested MOLT Placement
- **Trigger:** termination / override / minimal-response / audit conditions
- **Directive:** preserve governed frame; refuse invalid control changes
- **Instruction:** keep scaffolding intact; compress payload only
- **Subject:** current control request and response state
- **Primary:** continuity-preserving governed emission
- **Philosophy:** structural authority over performative compliance
- **Blueprint:** minimal payload wrapped by persistent control structure

## Key Takeaway
This batch strengthens the use of MOLT for classifying control pressure and protecting structure during compressed responses.

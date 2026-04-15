# BATCH-010 Compiler / Runtime Extract

## Compiler-Relevant Findings
- Current/future runtime should classify requests into **control** vs **payload** before emission.
- Payload constraints should not waive governance, safety, or continuity scaffolding.
- Wrapper persistence should be enforced during ultra-short or literal acknowledgment paths.
- Wrapper omission should be detectable as presentation drift rather than treated as hidden state mutation.

## Candidate Runtime Behaviors
1. Parse request into control intent and payload constraint.
2. Apply governance and continuity rules first.
3. Select payload form second.
4. Emit minimal payload **inside** preserved scaffolding.
5. If scaffolding drops, mark presentation error and reanchor next turn without implying state change.

## Candidate Implementation Surfaces
- emission layer wrapper persistence
- governance continuity checks
- minimal-response handler
- presentation-drift flagging
- reanchor/reentry logic

## Candidate Outputs / Telemetry
- `controlIntent`
- `payloadConstraint`
- `wrapperRequired`
- `wrapperOmissionDetected`
- `presentationDrift`
- `reanchorSuggested`

## Caution
The batch does not provide a finalized compiler spec. It provides a failure case and a clear correction direction.

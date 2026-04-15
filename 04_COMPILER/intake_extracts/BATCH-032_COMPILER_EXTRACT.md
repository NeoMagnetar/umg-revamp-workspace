# BATCH-032 — Compiler Extract

## Compiler-Relevant Findings
- the source proposes a bounded compiler/runtime guardrail rather than a large ontology expansion
- the preferred path is a small number of broad anchors plus a deterministic validator
- validation should occur before final answer emission and remain simple in failure handling

## Candidate Compiler Tasks
1. support minimal extension anchors:
   - TG
   - ROLES
   - ACT
   - U_TARGET
2. add `VALIDATE_GOAL_COHERENCE`
3. define bounded failure behaviors:
   - assumption-branch output
   - minimal clarification
   - conditional response
4. decide whether structured `SUB_PROFILE` belongs inside Subject or as a separate supported field

## Validation Targets From Source
- ACT satisfaction
- correct patient/entity handling
- TG preservation
- U_TARGET ordering

## Open Compiler Questions
- is validation a hard gate, a scoring penalty, or a threshold-trigger?
- should validator live inside MOLT compile flow or as a companion stage?
- how should overlap with Resolver/PrePass outputs be handled?
- how much of role binding needs to be explicit versus derived?

## Intake Position
Strong compiler evidence, but still provisional. This batch should inform a later compiler design comparison against resolver-first approaches before any canonical implementation decision.

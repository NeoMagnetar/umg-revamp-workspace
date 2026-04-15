# BATCH-011_COMPILER_EXTRACT

## Compiler / Runtime Signals
- Formal request pipeline is explicit:
  1. parse short MOLT skeleton
  2. determine relevant stacks
  3. apply governance
  4. select format blueprint
  5. emit output
- Runtime loop expands into:
  - GoalGenesis
  - GoalSelection
  - optional Plan/Execute
  - Output
  - Evaluate
  - Improve
  - Log

## Implementation-Relevant Signals
- governance precedes conflicting user requests
- format selection remains orthogonal to cognition/mode
- minimal payload can coexist with preserved structure
- bundle policy is operational, not cosmetic
- drift thresholds and rollback/promotion logic are part of bounded runtime behavior

## Candidate Compiler / Runtime Tasks
- formalize request parsing into MOLT -> stack selection -> governance -> blueprint -> emission
- preserve structural envelope under minimal-emission constraints
- implement governance lock enforcement in bounded-improvement pathways
- integrate bundle-expansion behavior from runtime spec
- support anti-thrash, review cadence, drift thresholds, rollback, and audit trace

## Limits / Uncertainty
- runtime agency loop is draft-stage
- safety layer is whitepaper-status
- merge behavior remains thinner than compiler/runtime ambition elsewhere

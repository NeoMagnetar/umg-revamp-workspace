# BATCH-001_SLEEVE_EXTRACT

## Extract Scope
Sleeve- and resleeving-specific evidence from the batch.

## Sleeve Signal
- Sleeve is treated as runtime identity.
- Sleeve is not reduced to a prompt preset or cosmetic label.
- Active sleeve state is distinct from both source files and compiled output.

## Resleeving Flow in Source
1. load sleeve source
2. compile
3. validate
4. snapshot old state
5. activate new sleeve / stacks / runtime

## Related Runtime Claims
- active sleeve state, active stack state, and runtime state are distinct artifacts
- runtime switching should be explicit
- resleeving should be deterministic, inspectable, and reversible

## Governance Context
- proof-of-concept sleeve remains intentionally permissive
- heavier governance remains conceptually separate and later-stage
- no final boundary rule is fixed in this batch

## Downstream Use
- sleeve documentation revision
- runtime contracts
- skill preflight rules for live-state activation

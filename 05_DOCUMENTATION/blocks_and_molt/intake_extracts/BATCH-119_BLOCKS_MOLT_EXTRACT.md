# BATCH-119_BLOCKS_MOLT_EXTRACT

## MOLT / Block Signal
- Core v0 MOLT type set extracted:
  - trigger
  - directive
  - instruction
  - subject
  - primary
  - philosophy
  - blueprint
- Global authority order extracted:
  - Trigger > Directive > Instruction > Subject > Primary > Philosophy > Blueprint

## Trigger Signal
- Trigger = named switch, not code
- trigger consideration and trigger-used-in-condition appear as trace events
- governance conditions can use triggerIdsAny and triggerIdsAll
- trigger merge is technically allowed but advanced / discouraged in v0

## Priority Signal
- priorityOrder is on Block
- higher value means stronger same-type priority
- priority is local and separate from authority

## Bundle Signal
- Bundle groups without changing meaning
- a block may be treated as a singleton bundle
- every block must belong to exactly one segment after normalization
- bundle use by type includes:
  - ranked directive sets
  - ranked rule sets
  - multi-focus subject grouping
  - primary alternates
  - layered philosophy
  - ordered blueprint segments

## Merge Signal
- Merge creates a new unit of meaning
- result must have a defined moltType
- sourceBlockIds / lineage must be preserved
- Primary merge is delicate and v0-discouraged
- compiler should not silently repair incompatible merges

## NeoBlock / NeoStack Signal
- each stack becomes one NeoBlock in simplest v0
- v0 simplest model also supports 1:1 stack -> NeoBlock -> NeoStack
- richer NeoStack semantics remain light / underdeveloped in this batch

## Sleeve / Executor Signal
- sleeve is main compiler input with TriggerState
- executor is downstream consumer of RuntimeSpec, not modifier of CIR/CSL artifacts

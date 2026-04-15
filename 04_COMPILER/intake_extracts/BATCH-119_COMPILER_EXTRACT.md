# BATCH-119_COMPILER_EXTRACT

## Canonical v0 Compiler Pipeline Extracted
- Step 0: inputs
- Step 1: basic validation
- Step 2: register and log triggers
- Step 3: normalize segments
- Step 4: apply governance
- Step 5: resolve stacks by authority + priority
- Step 6: resolve merge segments
- Step 7: construct NeoBlocks
- Step 8: construct NeoStacks
- Step 9: select primary
- Step 10: build RuntimeSpec
- Step 11: finalize Trace and result

## Validation Checks Extracted
- required fields
- type well-formedness
- ID uniqueness
- valid references
- governance bindings valid
- trigger references valid

## Segment Normalization Rules
- no overlapping segments on same block
- merge size must be >= 2
- all blocks assigned to a segment
- singleton bundles created implicitly when no explicit segment exists

## Trigger Compiler Boundary
- compiler does not compute triggers
- compiler only receives activeTriggerIds
- trigger evaluation is external

## Priority / Authority Logic
- authority works across MOLT types
- priority works within same-type competition
- higher priority wins same-type contradictions, with conflict_resolved trace logging
- governance may alter effective priority through prefer / override_priority

## Merge Policy Extracted
- merge creates a new unit of meaning
- merge must record lineage
- compiler does not invent new content
- unclear merge semantics -> reject merge or require explicit authored merged result
- Primary merge is v0-discouraged / effectively blocked

## Primary Selection Logic
- collect active Primary blocks after governance and merges
- multiple primaries in single stack outside Primary bundle -> error
- no primary globally -> error
- if multiple candidates:
  - governance
  - then priorityOrder
  - then first-defined tie-break
- alternatives stored separately

## Final Contracts
- runtime undefined if errors
- trace always returned
- hasErrors boolean always present
- same inputs -> same outputs at the specification layer

## Candidate Compiler Work
- implement locked v0 RuntimeSpec, Trace, and CompileResult schemas
- enforce segment normalization and singleton bundle generation
- enforce governance application with trigger-conditioned rules
- implement MOLT-specific merge policy and error paths
- implement deterministic tie-breaking and fail-closed behavior when required

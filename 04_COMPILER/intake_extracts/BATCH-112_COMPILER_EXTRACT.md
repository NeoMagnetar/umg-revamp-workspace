# BATCH-112 — Compiler Extract

## Compiler/runtime-facing signal
This batch introduces **CIR (Cognitive Intermediate Representation)** as a candidate representation layer for S2′ and ties it to a compile step that emits substrate-specific execution plans.

## Strong candidate compiler statements
- `compile(CIR, runtime) -> Plan`
- CIR is **representation**, not execution.
- Execution plans are **substrate-specific**.
- Governance and constraints are applied **upstream**.
- Runtime behavior should consume compiled cognition rather than invent cognition.

## Implications for compiler design
### Representation boundary
Compiler work may need a distinct layer that separates:
- cognition construction
- validation/governance
- compilation to execution plans
- runtime execution

### Potential pipeline pressure
Possible normalized pipeline implied by this batch:
1. construct cognition
2. validate/govern
3. represent as CIR
4. compile to execution plan
5. execute on target substrate
6. inspect/audit results

### Compatibility questions
This batch does **not** resolve whether CIR is:
- identical to a current UMG artifact,
- a new named layer,
- or a documentation veneer over existing runtime-spec outputs.

## Candidate tasks
- define CIR schema boundaries
- define CIR → execution plan compilation contract
- decide whether CIR is above, below, or equivalent to existing RuntimeSpec-like constructs
- define how governance/validation travel with CIR
- define cross-substrate compilation targets

## Caution
Do not promote graph/operator language or CIR language into implementation canon until it is reconciled with existing UMG block/stack/merge vocabulary.

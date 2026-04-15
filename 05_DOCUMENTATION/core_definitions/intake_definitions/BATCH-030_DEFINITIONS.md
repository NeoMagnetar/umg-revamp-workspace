# BATCH-030 — DEFINITIONS EXTRACT

## Terminology
### PrePass
- provisional name for a lightweight interpretation step that runs before MOLT mapping
- purpose: resolve objective, requirement, context, and priority before block selection fileciteturn6file0

### Resolver
- stronger / more formal candidate name for the pre-MOLT interpretation layer
- may emit a structured handoff object rather than direct final answers fileciteturn6file0

### `RESOLVER_OUTPUT.v1`
- proposed handoff object between interpretation and MOLT/compiler selection
- candidate fields mentioned in the source:
  - `objective_candidate`
  - `critical_requirement`
  - `context_frame`
  - `response_priority`
  - `literal_vs_implied_resolution`
  - `confidence_score`
  - `override_reason` fileciteturn6file0

### Interpretation Plane
- architectural plane responsible for framing the situation before MOLT fill
- concerned with objective, implied frame, and prerequisite conditions fileciteturn6file0

### Representation Plane
- architectural plane where structured MOLT mapping occurs after interpretation resolves the frame fileciteturn6file0

### Orchestration Plane
- architectural plane for ranking, arbitration, governance, and final composition/execution flow fileciteturn6file0

## Meaning Candidates
### Subject anchoring
- Subject should reflect the real-world center of the task, not simply the most obvious noun in the user’s wording. fileciteturn6file0

### Prerequisite-first rule
- If inferred objective and literal phrasing conflict, prerequisite reality should be checked first. fileciteturn6file0

### Literal override
- user intent may explicitly force literal treatment; this is a governance/control feature rather than the default interpretation path fileciteturn6file0

## Role Language
- MOLT remains the structured representation layer
- Resolver / PrePass is upstream interpretation
- compiler/runtime handles ranking, arbitration, and constraints fileciteturn6file0

## Architecture Language
- lean core MOLT
- selected extension families
- separated planes rather than ontology bloat
- interpretation before representation before orchestration fileciteturn6file0

## Runtime / Compiler Language
- `Input -> Resolver -> Candidate block generation -> Compiler ranking -> Apply constraints/governance -> Select final composition -> Emit`
- resolver output influences candidate generation and ranking rather than directly deciding the answer fileciteturn6file0

## Definitional Status
- all definitions in this file are evidence-stage extractions from a refinement-oriented source
- none should be treated as finalized canon without later synthesis and decision review

# BATCH-030 — COMPILER EXTRACT

## Compiler-Relevant Findings
### 1. New upstream interpretation interface
- The source argues for a lightweight Resolver / PrePass before MOLT block selection.
- This interface should rank likely objective, critical requirement, contextual frame, and literal-vs-implied interpretation. fileciteturn6file0

### 2. Formal handoff object candidate
- `RESOLVER_OUTPUT.v1` is proposed as the interface object between interpretation and MOLT/compiler selection.
- Candidate fields:
  - `objective_candidate`
  - `critical_requirement`
  - `context_frame`
  - `response_priority`
  - `literal_vs_implied_resolution`
  - `confidence_score`
  - `override_reason` fileciteturn6file0

### 3. Updated pipeline proposal
- `Input -> Resolver -> Candidate block generation -> Compiler ranking -> Apply constraints/governance -> Select final composition -> Emit` fileciteturn6file0

### 4. Ranking logic signal
- Priority should not be treated as surface token emphasis alone.
- Objective-critical requirement outranks likely objective; literal wording can be outranked by prerequisite reality. fileciteturn6file0

## Compiler Impact Candidates
- add resolver stage before candidate selection
- define ranking semantics for prerequisite-first logic
- expose literal-override path
- keep resolver advisory so compiler remains final arbitration layer
- benchmark framing errors separately from downstream MOLT execution errors fileciteturn6file0

## Risks
- naming and packaging are unresolved
- question count for the resolver is not finalized
- scope creep risk if too many new cognitive functions are promoted into equal-status formal families fileciteturn6file0

## Recommended Hold Position
Treat this batch as strong evidence for compiler design direction, but not yet as a final implementation contract. fileciteturn6file0

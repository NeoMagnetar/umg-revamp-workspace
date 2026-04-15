# BATCH-030 — PREPASS_RESOLVER_AND_INTERPRETATION_LAYER_REVIEW

## Batch Overview
- **Batch ID:** BATCH-030
- **Short Topic:** PrePass / Resolver and pre-MOLT interpretation
- **Source Type:** derivative summary artifact, not raw transcript
- **Review Status:** REVIEWED
- **Disposition:** ACCEPT_AS_EVIDENCE / NOT_CANON
- **Primary Domain:** core semantics + compiler/runtime framing
- **Source Basis:** attached summary file fileciteturn6file0

## Source Snapshot
- The source begins with a trivial practical question and uses the resulting reasoning failure as a diagnostic case.
- The conversation then proposes a lightweight pre-MOLT interpretation layer that resolves real objective, critical requirement, contextual frame, and priority before MOLT mapping.
- It expands into a broader UMG 2.0 architecture synthesis that separates interpretation, representation, and orchestration planes. fileciteturn6file0

## Chat-Level Summary
This batch argues that some failures attributed to MOLT actually occur earlier, when the model locks onto literal wording instead of the real task center. The proposed fix is a lightweight Resolver / PrePass layer that runs before MOLT and ranks likely objective, prerequisite conditions, contextual frame, and response priority. The source also warns against inflating the MOLT ontology by promoting every useful cognitive function into an equal-status block family, favoring a lean core plus cleaner separation of architectural planes. fileciteturn6file0

## UMG-Relevant Extraction
### 1. Pre-MOLT interpretation as a distinct function
- MOLT is framed as working best **after** the task has been correctly resolved.
- The failure mode is identified as upstream framing error, not a flaw in structured representation itself.
- This yields a new architectural boundary: interpretation first, representation second. fileciteturn6file0

### 2. Resolver / PrePass candidate design
- The lightweight version asks a small set of internal questions before MOLT fill:
  - likely real-world objective
  - most critical requirement or constraint
  - whether literal wording fully captures the situation or whether a stronger implied frame exists
- A more formal handoff object is proposed as `RESOLVER_OUTPUT.v1`. fileciteturn6file0

### 3. Priority and prerequisite-first discipline
- The batch introduces a priority ordering where objective-critical requirement outranks likely objective, which outranks context frame, which outranks literal wording, which outranks incidental detail.
- The canonical example is the car wash case: the car must be present before any walk-versus-drive efficiency analysis matters. fileciteturn6file0

### 4. Three-plane architecture signal
- The source recommends separating:
  - **Interpretation Plane**
  - **Representation Plane**
  - **Orchestration Plane**
- This is meant to improve correctness without ontological bloat. fileciteturn6file0

### 5. Compiler/runtime implications
- Recommended flow becomes:
  `Input -> Resolver -> Candidate block generation -> Compiler ranking -> Apply constraints/governance -> Select final composition -> Emit`
- Resolver output is advisory/ranking-oriented, not a direct answer generator. fileciteturn6file0

## Independent Review
This is a high-value batch for the revamp because it isolates a specific failure class and converts it into a clean architectural proposal. The strongest contribution is not merely “add another block,” but “separate framing from representation.” That distinction could materially reduce shallow literal misreads across the whole system if implemented carefully.

Important caution: the source is still exploratory on packaging details. It does **not** finalize whether the new logic should be called PrePass, Resolver, meta-layer, or wrapper stack, and it does **not** fully settle question count or plane boundaries. The evidence is therefore strong for direction and candidate canon language, but not yet sufficient for final canonical implementation rules. fileciteturn6file0

## Roadmap Mapping
### Primary phase impact
- **PHASE_1_CORE_ALIGNMENT**
  - clarifies that MOLT should remain lean and should not absorb all upstream interpretation work
  - introduces candidate canon around subject anchoring and prerequisite-first reasoning

### Secondary phase impact
- **PHASE_2_COMPILER_IMPACT**
  - suggests a resolver object, ranking interface, and updated compiler pipeline
- **PHASE_3_DOCUMENTATION_IMPACT**
  - implies new documentation for interpretation vs representation vs orchestration
- **PHASE_5_PRD_AND_STAGING**
  - suggests implementation order: fix framing first, then selective expansion

## Action Outcome
- Accepted as evidence for:
  - PrePass / Resolver architecture direction
  - prerequisite-first interpretation rule
  - three-plane separation language
  - lean-core anti-bloat design pressure
- Not promoted to canon.
- Optional extracts justified:
  - compiler extract
  - blocks/MOLT extract

## Recommended Next Decision
Decide whether the pre-MOLT layer should be canonized as a named **Resolver/PrePass interface** with a formal handoff object, or whether its functions should remain partially distributed between compiler ranking and lightweight pre-interpretation policy.


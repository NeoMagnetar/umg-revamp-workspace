# BATCH-032 — MOLT Minimal Extension Framework Review

## Batch Overview
- **Batch ID:** BATCH-032
- **Short Topic:** MOLT minimal extension framework
- **Source Type:** derivative summary of prior chat, not raw transcript
- **Stage:** Stage 1 intake only
- **Status:** reviewed as evidence, not canon
- **Disposition:** ACCEPT_AS_EVIDENCE

## Source Snapshot
- Source centers on a repeated car-wash reasoning failure and uses it to diagnose goal–means misbinding inside current MOLT handling.
- The chat does **not** reject MOLT. It argues for a lightweight schema upgrade that preserves MOLT’s minimalism while improving teleological accuracy.
- The endpoint is a cross-model proposal named **MOLT Minimal Extension Framework (MMEF v0.1)**, positioned for cooperative review rather than unilateral canon adoption.

## Chat-Level Summary
The batch argues that MOLT can fail when it binds surface logistics before terminal purpose. The proposed repair is intentionally small: use a few broad semantic anchors such as terminal goal, role binding, activation constraint, and utility ordering, then run one deterministic goal-coherence validation pass before final answering. The source repeatedly resists ontology bloat and prefers a minimal compiler-safe extension path.

## UMG-Relevant Extraction
### Core signal
- MOLT remains the structured representation layer.
- The weakness identified is **goal–means misalignment** before or during structured binding.
- The proposed repair is **minimal extension + single validation pass**, not large family proliferation.

### Candidate extension anchors
- **TG / Terminal Goal** — what the system is ultimately trying to accomplish.
- **ROLES** — actor/object/agent/patient/instrument style semantic role binding.
- **ACT / Activation Constraint** — preconditions or operational constraints that must be satisfied.
- **U_TARGET / Utility ordering** — explicit optimization order such as correctness > safety > time > friction.
- Optional structured **SUB_PROFILE** is explored as a possible way to enrich Subject without broad taxonomy explosion.

### Runtime / compiler direction
- Add a deterministic validator such as `VALIDATE_GOAL_COHERENCE`.
- Validator checks:
  - whether activation conditions are satisfied
  - whether the correct patient/entity is being acted on
  - whether terminal goal is preserved
  - whether explicit utility ordering is being respected
- Failure behavior should stay bounded:
  - branch with assumptions
  - ask minimal clarification
  - return conditional outputs

### Design doctrine from source
- broad types > narrow proliferation
- validation pass > semantic bloat
- no recursive inference
- no semantic explosion
- keep portability and compiler feasibility

## Independent Review
This is strong evidence for a **lean-evolution** path rather than a maximal ontology path. The batch is especially valuable because it does not merely complain about an error; it translates the error into a bounded architectural response with specific proposed fields and a validation gate. It also complements BATCH-030: where BATCH-030 argues for framing/Resolver separation, this batch sharpens a **minimal internal schema extension** path for goal coherence inside or adjacent to MOLT.

The source is still provisional. Several candidate roles are explored before being narrowed, and the exact runtime behavior of validation remains unresolved. The batch should therefore remain in evidence status until compared against other framing/prepass material and any existing canonical Subject/Need/Aim rules.

## Roadmap Mapping
### Primary phases touched
- **PHASE_1_CORE_ALIGNMENT**
  - clarifies how terminal goal, role binding, and utility ordering might relate to existing MOLT semantics
- **PHASE_2_COMPILER_IMPACT**
  - proposes a deterministic validation stage and minimal extension anchors
- **PHASE_3_DOCUMENTATION_IMPACT**
  - supports documentation around terminal vs instrumental goal and bounded extension philosophy
- **PHASE_5_PRD_AND_STAGING**
  - provides a lightweight candidate evolution path rather than full family explosion

### Cross-batch relation
- overlaps with BATCH-030 on framing and prerequisite-first handling
- more focused than BATCH-030 on **minimal schema anchors** and validator design
- likely duplicate pressure with any prior notes on teleology, subject anchoring, or role sufficiency

## Action Outcome
- retained as Stage 1 evidence
- frozen into a compact intake pack
- optional extracts added because the source is dense on compiler and MOLT-extension surfaces
- no canon promotion performed

## Recommended Next Decision
Decide whether the current project should treat **goal coherence** primarily as:
1. a PrePass/Resolver responsibility,
2. a minimal MOLT-extension responsibility,
3. or a split responsibility with resolver framing plus compiler validation.

A second linked decision is whether **Subject** should be enriched internally or whether the cleaner path is separate explicit anchors like TG, ROLES, ACT, and U_TARGET.

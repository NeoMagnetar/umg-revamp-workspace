# BATCH-002 — PUBLIC COMPILER REVIEW

## Batch Overview
- **Batch ID:** BATCH-002
- **Short Topic:** public compiler review / semantic drift / patch sequencing
- **Source Type:** chat-derived structured summary
- **Evidence Status:** non-canon intake evidence
- **Primary Domain:** compiler contract and semantic enforcement
- **Optional Extracts Included:** compiler extract
- **Disposition:** export as Stage 1 evidence pack

## Source Snapshot
- The batch reviews the publicly visible `umg-compiler` build and treats it as the accessible evidence surface.
- The private Replit / UMG Studio compiler is explicitly out of view in this batch.
- The source focuses on current compiler behavior, semantic weakness points, and the correct order for future patching.
- The source repeatedly distinguishes observed public behavior from inferred broader UMG direction.

## Chat-Level Summary
This batch is a compiler-focused intake source. It treats the compiler as a deterministic structural layer that validates, normalizes, merges, applies governance, resolves active content, and emits runtime-facing artifacts. The strongest finding is not that the compiler is invalid, but that it may be lagging behind broader UMG semantic evolution. The batch identifies likely weak points around priority consistency, governance propagation, activation guarantees, hierarchy strength, and contract drift between public implementation and broader UMG intent. It recommends a staged path: stabilize canon first, define the compiler contract second, patch implementations third, then verify public/private parity.

## UMG-Relevant Extraction
### Structural role of the compiler
- The compiler is treated as a real structural compiler, not a cosmetic prompt formatter.
- It compiles sleeve-like JSON into runtime-facing artifacts.
- The interpreted public flow is:
  - validate references and schema
  - normalize segments
  - apply merges
  - record/apply bundles
  - apply governance
  - resolve authority and ordering
  - select active blocks by role
  - emit runtime artifacts

### Semantic tension identified
- The public compiler appears more aligned to the older fixed seven-role MOLT model.
- Broader UMG direction may be moving toward richer staged orchestration.
- This possible drift is not resolved in the batch; it remains an evidence signal.

### High-signal defect / weakness areas
- Priority semantics may be inconsistent across sort order, alternates, selectors, and governance effects.
- Governance effects may not propagate consistently across all selection paths.
- `require` behavior may be too weak, acting more like existence validation than activation guarantee.
- `limit` behavior may exist conceptually but not be strongly enforced during runtime selection.
- Hierarchy may be implemented more as positional order than strong causal dependency.
- Primary selection may be weaker than other selector paths.

### Patch sequencing logic
- Do not patch blind.
- Lock canonical semantics first.
- Define or revise the compiler contract second.
- Patch implementation third.
- Align public/private builds and tests afterward.

## Independent Review
This is a strong Stage 1 compiler evidence source because it does three useful things at once: it validates that the public compiler is already substantial, isolates probable structural weakness points, and keeps unresolved architecture questions separate from observed behavior. The source is careful not to pretend that newer MOLT types, pre-pass, or stronger hierarchy semantics are finalized. That makes it useful for intake because it preserves evidence without premature canonization.

The batch is especially valuable for revamp work because it frames the compiler problem as a contract-alignment problem, not a rewrite-from-zero problem. That reduces noise and points the control project toward semantic stabilization and parity testing. The main caution is that some conclusions are inferential from public behavior and summaries, not confirmed against the private compiler or a finalized semantic spec.

## Roadmap Mapping
- **Phase 1 — Core Alignment:** strong impact
  - current MOLT taxonomy
  - hierarchy meaning
  - governance semantics
  - priority semantics
- **Phase 2 — Compiler Impact:** very strong impact
  - selector logic
  - governance propagation
  - activation guarantees
  - parity testing
- **Phase 3 — Documentation Impact:** medium-strong impact
  - compiler contract language
  - migration notes
  - pre-pass clarification
- **Phase 4 — Skill Alignment:** medium impact
  - preserve portable compiler retrospectives for agent handoff
- **Phase 5 — PRD and Staging:** medium impact
  - canon → contract → implementation → parity/test sequence

## Action Outcome
- Accept as evidence.
- Freeze as a reviewed compiler-oriented intake batch.
- Extract compiler-specific findings into a dedicated optional file.
- Do not promote any candidate statements to canon from this batch alone.
- Hold unresolved items for later semantic alignment.

## Recommended Next Decision
Lock the canonical compiler contract boundary:
1. whether the seven-role MOLT model is still the active top-level compiler contract,
2. whether pre-pass is part of the compiler contract,
3. whether hierarchy is positional, dependency-gated, or both,
4. what `require`, `prefer`, and `limit` must guarantee operationally.

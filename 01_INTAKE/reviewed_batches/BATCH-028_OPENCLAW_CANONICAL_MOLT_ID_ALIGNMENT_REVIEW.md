# BATCH-028 — OpenClaw Canonical MOLT ID Alignment Review

## Batch Overview
- **Batch ID:** BATCH-028
- **Short Topic:** Canonical MOLT ID alignment for OpenClaw routing architecture
- **Review Status:** REVIEWED
- **Disposition:** ACCEPT_AS_EVIDENCE / NOT_CANON
- **Source Type:** derived intake summary rather than raw transcript
- **Evidence Boundary:** treat all extracted material as draft/refinement evidence, not canon

## Source Snapshot
- The batch is a read-and-confirm / refinement thread about existing OpenClaw routing and sleeve design artifacts.
- The visible source references a GitHub orchestrator sleeve, a broader mode-router sleeve, and a repo-analysis neostack.
- The only direct refinement instruction is narrow: future work should stop inventing random trigger numbering and should align with canonical MOLT blocks already present in GitHub/project files.

## Chat-Level Summary
This batch does not primarily introduce a new sleeve architecture. Its main value is a control correction. It says that sleeve and neostack drafting should be anchored to the existing canonical MOLT library, not to improvised identifiers. It also reaffirms deterministic routing discipline, explicit model binding at stack entry, and auditable transitions between sleeve, neostack, and execution stages.

## UMG-Relevant Extraction
### Structural hierarchy
- Reaffirms **Block -> NeoBlock -> NeoStack -> Sleeve**.
- Reaffirms sleeve as router/governor layer and neostack as executable task mode.
- Reaffirms that neostacks should be built from known MOLT atoms rather than ad-hoc structures.

### Trigger / routing discipline
- Trigger resolution is treated as the first routing gate.
- Clean routing is preserved as: **Trigger -> Neostack -> Directive -> Instruction -> Execution -> Verify -> Report**.
- Random trigger numbering is explicitly treated as a flaw when canonical trigger blocks already exist.

### Canonical ID discipline
- NeoBlocks should reference canonical MOLT IDs already present in project files.
- Future spec work should not invent identifiers where existing block IDs are available.
- Compiler/tooling compatibility is implied as a direct reason for this discipline.

### Compiler / runtime implications
- Runtime flow is staged and explicit rather than improvised.
- Canonical naming and reference discipline are treated as prerequisites for clean compilation and reliable tooling resolution.
- Model binding at stack entry is preserved as part of the runtime contract.

### Documentation / workflow implications
- The workflow model is: read existing canon, acknowledge it, then refine against the canonical block set.
- Draft examples may be structurally useful but still require identifier normalization before compiler-aligned use.

## Independent Review
This batch is high value as a refinement-control artifact, but lower value as a source of finalized substantive semantics. Much of the visible chat is read-confirmation rather than new resolved design work. Its strongest contribution is the explicit discipline that canonical MOLT IDs should be reused and that structural examples must be normalized before they are treated as compiler-ready. That is important for Phase 1 and especially Phase 2, but it should not be promoted to canon without cross-checking against the actual block inventory and any existing naming rules.

## Roadmap Mapping
### Primary phase touches
- **PHASE_1_CORE_ALIGNMENT**
  - supports deterministic Trigger semantics
  - supports disciplined NeoBlock composition expectations
- **PHASE_2_COMPILER_IMPACT**
  - directly implies block-ID validation and normalization requirements
- **PHASE_3_DOCUMENTATION_IMPACT**
  - implies spec examples should prefer canonical IDs
- **PHASE_4_SKILL_ALIGNMENT**
  - implies sleeve-generation skills should default to canonical block lookup
- **PHASE_5_PRD_AND_STAGING**
  - useful as staging evidence for compiler-aligned sleeve design workflow

### Duplicate pressure
- High overlap with earlier sleeve / router batches on deterministic architecture.
- Distinctive value is the explicit anti-random-ID correction.

### Contradiction watch
- Minor terminology drift appears (`NST.` vs `NSTK.`).
- No hard contradiction is resolved in the visible source.

## Action Outcome
- Accept as **evidence**.
- Do **not** promote to canon.
- Freeze as Stage 1 pack because the refinement doctrine is coherent enough to preserve as an artifact.
- Route compiler-facing and blocks/MOLT-facing extracts to their intake destinations.

## Recommended Next Decision
Determine whether the project should adopt an explicit rule that all future neostack/spec examples must reference canonical MOLT IDs when available, with normalization required before any draft is considered compiler-ready.

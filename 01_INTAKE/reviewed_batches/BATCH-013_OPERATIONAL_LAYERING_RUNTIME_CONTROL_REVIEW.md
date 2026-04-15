# BATCH-013_OPERATIONAL_LAYERING_RUNTIME_CONTROL_REVIEW

## Batch Overview
- **Batch ID:** BATCH-013
- **Short Topic:** operational layering / runtime control
- **Disposition:** EXPORT_CANDIDATE
- **Evidence Status:** non-canon Stage 1 intake evidence
- **Primary Domain:** governance-sleeve-runtime layering

## Source Snapshot
- Source type: extracted chat summary with surfaced project artifacts
- Main scope:
  - governance vs sleeve vs output vs runtime control
  - project files vs project instructions vs conversation runtime
  - tri-state stack control and bounded runtime mutation
  - copy-friendly renderer/output canon separation
  - library/spec creation and surfaced runtime/safety documents
- Source posture: operational design and hardening, not final canon

## Chat-Level Summary
This batch operationalizes UMG inside ChatGPT as a layered control system rather than a single prompt. The chat separates governance, sleeve identity, NeoStacks, NeoBlocks, Blocks, MOLT, and output rendering into distinct layers, then proposes a concrete deployment pattern: governance and sleeves in project files, output canon in project instructions, and session-local runtime mutation in conversation. It also introduces tri-state stack control (OFF / ON / ADAPTIVE), registry-based runtime state tracking, bounded creation of runtime Blocks / NeoBlocks / NeoStacks, and explicit promotion requirements before any session-local work becomes canon.

## UMG-Relevant Extraction
### Core signal
- Governance is above sleeve behavior and output rendering.
- Sleeves define active operating configuration inside allowed space.
- Output canon is presentation-only and must not be confused with authority.
- Project files hold canonical libraries and base sleeve/governance artifacts.
- Project instructions hold stack policy and renderer rules.
- Conversation runtime holds validated, session-local registries and mutations.

### High-value structures
- **Tri-state stack control**
  - `OFF` = unavailable and not self-enableable
  - `ON` = available and usable
  - `ADAPTIVE` = available, locally toggleable if policy allows
- **Session registries**
  - stack registry
  - neoblock registry
  - delta log
- **Mutation policy**
  - no mid-turn mutation
  - validate before apply
  - apply next turn only
  - session-local unless explicitly promoted
- **Composition refinement**
  - Block = single MOLT-role unit
  - NeoBlock = full MOLT stack
  - NeoStack = capability grouping / domain aggregation
- **Renderer separation**
  - output canon shapes presentation only
  - governance shapes permission and authority
  - presentation lapse should be treated as `PRESENTATION_ERROR_ONLY`

## Independent Review
### What this batch adds
- A concrete operating split between canon storage, policy layer, and runtime layer.
- A more precise runtime-control model than earlier broad sleeve descriptions.
- A practical path for allowing bounded assistant agency without collapsing governance.
- A durable clarification that output structure is renderer-only and should not absorb authority logic.

### What remains provisional
- Detailed deterministic compiler behavior for merge and bundle is not finalized here.
- Exact edge-case wording for assistant-controlled adaptive toggling remains unfinished.
- Runtime sleeve switching exists conceptually, but no full compiler-grade sleeve-switch path is finalized.
- Operational stability lagged behind architecture clarity in parts of the chat.

### Duplicate pressure
- Strong overlap with prior batches on:
  - governance precedence
  - output vs cognition separation
  - bounded runtime mutation
  - project-file-based sleeve architecture
- Distinctive contribution here is the explicit control-plane split:
  - project files
  - project instructions
  - runtime session registry

## Roadmap Mapping
- **Phase 1 — Core Alignment**
  - governance vs sleeve vs renderer separation
  - Block vs NeoBlock role refinement
  - stack availability semantics
- **Phase 2 — Compiler Impact**
  - validate `STACK_CONTROL` and `SLEEVE_CONTROL`
  - staged next-turn application
  - registry maintenance
  - lock/dependency checks
- **Phase 3 — Documentation Impact**
  - renderer-only output canon
  - project/runtime layer map
  - snapshot rendering for real NeoBlocks
- **Phase 4 — Skill Alignment**
  - project/library loading workflow
  - bounded block reconfiguration skill
- **Phase 5 — PRD and Staging**
  - project files as canon sources
  - runtime mutation remains session-local until promotion

## Action Outcome
- Accepted as evidence for:
  - control-plane separation
  - bounded adaptive stack policy
  - runtime mutation rules
  - renderer-only output canon
- Strong export candidate for compiler/spec/docs alignment.
- Not canonized in this batch.

## Recommended Next Decision
Lock the architectural boundary between:
1. project-file canon,
2. project-instruction policy,
3. session-local runtime mutation and registries.

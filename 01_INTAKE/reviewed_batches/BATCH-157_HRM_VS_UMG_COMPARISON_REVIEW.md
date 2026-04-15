# BATCH-157 — HRM vs UMG comparison review

## Batch Overview
This batch captures a comparison between HRM and UMG that gradually shifts from conceptual comparison into a concrete integration pattern. The source treats UMG as an orchestration architecture rather than a single model, then proposes HRM as a specialist latent solver wrapped inside a UMG-controlled execution path. The strongest signal is not benchmark comparison by itself, but the operational pattern of using UMG as the governing wrapper around an external reasoning engine.

## Source Snapshot
- Source type: pasted chat summary / extraction batch
- Primary subject: HRM vs UMG comparison with implementation path
- Secondary subject: local GPU readiness, WSL2 / CUDA prerequisites, ARC submission path
- Structural output in source: semantics framing, role mapping, wrapper proposal, runtime control pattern, staged deployment path

## Chat-Level Summary
The chat began as research into HRM and then moved into a structured comparison against UMG. From there it shifted into implementation: whether HRM could run locally on the user’s machine, how UMG could wrap HRM, what runtime / adapter files would be needed, and how that combined path could lead to ARC submission. The most project-relevant move is the framing of UMG as a model-agnostic orchestration layer that can route to a specialist solver while preserving audit, verification, and control.

## UMG-Relevant Extraction
### Core signal
- UMG is framed as an orchestration architecture / modular thought architecture / systems wrapper rather than a single model.
- HRM is framed as a compact latent reasoner suitable for specialist puzzle-style solving.
- The comparison proposes a division of labor where UMG governs routing, verification, budget, and fallback while HRM performs narrow solver work.

### Role mapping signal
- Directive / Blueprint = planning / strategy route selection.
- Primary / Subject = execution surface.
- Verifier = post-execution checking, self-consistency, majority vote, and bounded retry logic.

### Integration signal
- Candidate wrapped unit: `hrm.solver`
- Candidate wrapper files: `hrm_cli.py`, `hrm.config.json`, `adapter.ts`
- Candidate invocation model: UMG chooses HRM selectively for ARC-like or grid-logic tasks, then verifies outputs through a UMG-level audit layer.

### Runtime / control signal
- UMG sets compute budget, retry policy, fallback routes, and confidence gates.
- UMG can add an explainability shim exposing halt decisions, loop counts, and vote tallies.
- The source implies a runtime pattern where latent reasoning remains inside the specialist solver while explicit audit remains at the orchestration layer.

### Staging signal
- Confirm GPU / CUDA / WSL2 readiness.
- Install and validate HRM locally.
- Wrap HRM in a UMG-facing module and metadata layer.
- Run ARC-style evaluation.
- Package an offline submission path for Kaggle or similar constraints.

## Independent Review
This is strong evidence for how UMG may absorb an external specialist reasoner without surrendering its own architectural identity. The batch is valuable because it keeps UMG positioned as the coordinating layer and does not collapse UMG into the solver being wrapped. It contributes meaningful language for semantics, documentation, runtime design, and deployment workflow.

The main caution is that some of the strongest terms remain provisional:
- `hrm.solver` is a proposed name, not an approved canonical unit.
- block / nCube / solver module are used around the same idea without normalization.
- the comparison includes positioning language and operational proposals, not confirmed implementation.
- the environment-readiness side of the workflow remains unresolved until actual GPU / CUDA validation happens.

## Roadmap Mapping
- **Phase 1 — Core Alignment:** useful for clarifying whether UMG should be described as orchestration architecture, modular thought architecture, systems wrapper, or some normalized combination.
- **Phase 2 — Compiler Impact:** relevant for routing logic, invocation contracts, verifier hooks, trace surfaces, and adaptive retry governance.
- **Phase 3 — Documentation Impact:** relevant for describing external specialist reasoners, explicit audit surfaces, and planning/execution/verification distinctions.
- **Phase 4 — Skill Alignment:** relevant for adapter patterns, local solver execution skills, and operator-surface separation.
- **Phase 5 — PRD and Staging:** relevant for staged integration path from hardware readiness through wrapped runtime and submission packaging.

## Action Outcome
- Disposition: `ACCEPT_AS_EVIDENCE`
- Promotion status: not canon
- Immediate value: semantics framing, wrapper pattern, runtime control model, staging path
- Recommended next decision: normalize the UMG term for wrapped external reasoning units before compiler or documentation hardening proceeds

## Checklist Update Block
- Evidence retained for semantics alignment: yes
- Evidence retained for compiler/runtime design: yes
- Evidence retained for documentation revision: yes
- Evidence retained for skill alignment: yes
- Evidence retained for PRD/staging: yes
- Contradiction file required: no

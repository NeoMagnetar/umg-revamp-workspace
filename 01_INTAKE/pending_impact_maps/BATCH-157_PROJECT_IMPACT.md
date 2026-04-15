# BATCH-157 — Project Impact Map

## Primary Impact
This batch impacts the project most strongly at the semantics, runtime-routing, and documentation layers. It gives a concrete example of how UMG can remain the orchestrator while integrating a strong but narrow external reasoning engine.

## Roadmap Impact by Phase
### Phase 1 — Core Alignment
- reinforces the need to define UMG at the systems level, not as a single-model identity
- raises a terminology decision: wrapped unit = block, nCube, solver module, or other canonical type
- sharpens the planning / execution / verification distinction

### Phase 2 — Compiler Impact
- candidate routing logic for specialist solver dispatch
- candidate verifier integration for confidence-gated retries
- candidate trace outputs: halt decisions, loop counts, vote tallies
- candidate standardized invocation contract for wrapped modules

### Phase 3 — Documentation Impact
- candidate phrasing for orchestration architecture, modular thought architecture, and systems wrapper
- candidate guidance on wrapping latent specialist engines inside explicit audit layers
- candidate comparison note on latent reasoning vs explicit orchestration

### Phase 4 — Skill Alignment
- candidate adapter skill for Python / WSL-based local solver invocation
- candidate workflow doc update separating voice-helper surfaces from direct execution surfaces
- candidate local evaluation / verification skill flows

### Phase 5 — PRD and Staging
- stage 1: GPU / CUDA / WSL2 readiness
- stage 2: HRM install and validation
- stage 3: UMG wrapper integration
- stage 4: ARC-like evaluation
- stage 5: offline submission packaging

## Dependencies / Preconditions
- actual hardware / driver verification remains unresolved
- canonical naming for wrapped external modules is still open
- UMG-level verifier boundaries vs solver-internal voting remain unresolved

## Recommended Next Decision
Decide the canonical abstraction for an external specialist reasoning unit before broader wrapper conventions are documented or staged for implementation.

## Disposition
`ACCEPT_AS_EVIDENCE`

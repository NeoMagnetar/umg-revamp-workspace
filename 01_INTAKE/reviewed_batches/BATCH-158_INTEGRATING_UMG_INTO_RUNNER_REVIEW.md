# BATCH-158 — Integrating UMG into Runner — Review

## Batch Overview
This source batch presents an implementation-oriented integration pattern for mounting UMG into an existing Agentic Runner. The core claim is that UMG should not replace the runner substrate; instead, it should provide doctrine, planning, validation, guards, overlays, sleeves, and middleware on top of the runner’s existing queue, worker, and tool execution surfaces.

## Source Snapshot
- Source type: pasted chat summary / extraction batch
- Main subject: UMG integration into an Agentic Runner
- Orientation: implementation scaffold plus doctrinal framing
- Evidence quality: strong for architectural patterning and runtime decomposition; provisional for exact implementation because the generated starter pack is a scaffold, not verified live integration

## Faithful Source Summary
The chat framed UMG as a modular cognitive/control layer that sits between task intake and tool execution. It proposed a three-layer architecture:
1. Agentic Runner
2. UMG Adapter Layer
3. UMG Kernel

Within that framing, UMG provides MOLT planning, CEL action orchestration, VSS validation gates, Guards for bounded execution, and Overlays/Sleeves for runtime modulation. The chat then translated those ideas into concrete implementation primitives such as typed runtime contracts, plan synthesis, action loops, guard decisions, tool specs, middleware, eventing, memory hooks, and stop/redirect control. It also extended the integration with user-specific vault/alignment material, hooks, overlays, sleeves, and triggers, and ended by generating a starter zip scaffold for plugging into the user’s runner.

## UMG-Relevant Extraction
### Strong Signals
- UMG is treated as doctrine/control mounted into an execution runtime rather than as a replacement runtime.
- UMG is mapped into a concrete kernel vocabulary: MOLT, CEL, VSS, Guards, Overlays.
- Typed contracts appear as a candidate runtime interface layer.
- Bounded agency is implemented through guards, budget caps, validation checkpoints, and inert demo stubs.
- Sleeves and overlays are configuration surfaces that modulate behavior without replacing the underlying execution loop.
- The source includes explicit trigger and memory-rewrite semantics in scaffold form.

### High-Value Structural Pattern
The most important pattern is:
- runner = execution muscle
- UMG adapter = glue layer
- UMG kernel = planning, doctrine, validation, and bounded control

This is stronger than a prose-only positioning claim because the source also attaches contracts, folder structure, middleware, hooks, and starter packaging.

## Independent Review
This batch is high-value Stage 1 evidence for implementation-oriented UMG architecture. It is especially useful because it operationalizes several UMG concepts at once:
- doctrine/control
- runtime contracts
- middleware injection
- sleeves/overlays as configuration
- bounded execution through guards and VSS checks
- starter-pack export discipline

The strongest evidence contribution is not the specific demo runner but the architectural relationship between a host runtime and a UMG control layer. That relationship is consistent with a workable agent-ready release direction because it supports modularity, auditability, and controlled execution.

## Roadmap Mapping
### Phase 1 — Core Alignment
Relevant for clarifying how MOLT, CEL, VSS, Guards, and Overlays map into a runtime system.

### Phase 2 — Compiler Impact
Relevant for typed plan compilation, node-boundary control, overlay-to-runtime translation, and capability-based tool resolution.

### Phase 3 — Documentation Impact
Relevant for documenting the three-layer architecture and explaining UMG as a control layer rather than a substrate replacement.

### Phase 4 — Skill Alignment
Relevant for runner-facing skills, tool bus adapters, and closed-loop validation flows.

### Phase 5 — PRD and Staging
Relevant for staging an “integration v0” artifact path and defining observability/deployment gates.

## Disposition
**ACCEPT_AS_EVIDENCE**

Rationale:
- The source is coherent and implementation-oriented.
- It contains a practical integration pattern rather than isolated phrases only.
- It remains non-canonical because parts of the scaffold are provisional, user-specific, or intentionally inert.

## Cross-File Synthesis Note
This batch strengthens a recurring project theme from recent batches:
- UMG adds control, verification, structure, and bounded agency around an execution environment or specialist substrate.
- It does not need to replace the substrate to be architecturally central.

## Recommended Next Decision
Hold for later synthesis against:
- bounded agency / handoff bundle pattern
- local runtime / protocol boundary pattern
- external solver wrapper pattern
- block/schema and runner integration architecture

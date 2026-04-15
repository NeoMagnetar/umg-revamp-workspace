# BATCH-171 UMG Design Considerations — Review

## Batch Overview
- **Batch ID:** BATCH-171
- **Source Title:** 171 UMG design considerations
- **Disposition:** ACCEPT_AS_EVIDENCE
- **Confidence:** Medium
- **Primary Value:** Runtime semantics and composition logic for UMG blocks, especially trigger-driven activation, merge priority, snap-fit mechanics, philosophy/overlay behavior, and an implementation-oriented event pipeline.

## Source Snapshot
This source begins from screenshot-derived questions about UMG architecture and then develops those questions into a more implementation-oriented model. The strongest signals are:
- block hierarchy and merge priority
- snap-fit mechanics across vertical and horizontal axes
- trigger-driven activation behavior
- philosophy/ethics as runtime-shaping overlays
- a provisional runtime bus of event → arbiter → scheduler → executor → merger → auditor

The source is partly interpretive because the screenshot text was only partially visible and the later runtime model extends beyond the exact visible phrasing.

## Chat-Level Summary
The chat moved from interpretation into proto-specification. It first grouped visible screenshot themes into snap-fit, trigger behavior, philosophy blocks, runtime behavior, and theoretical-versus-implementation framing. It then translated those into a concrete UMG execution sketch in which:
- triggers activate directive sets
- directives organize instruction layers
- overlays/philosophy apply filtering and constraints
- foundations provide execution support
- an arbiter/scheduler/executor/merger/auditor chain governs runtime

This makes the batch useful for semantics, compiler/runtime modeling, and documentation, but the implementation-oriented answers remain proposals rather than ratified canon.

## UMG-Relevant Extraction
### Strongest signals
1. **Priority and conflict-resolution**
   - Screenshot-grounded hierarchy emphasized `Trigger > Directive > Instruction`.
   - Later proposed extension: `Trigger > Directive > Instruction > Overlay > Blueprint > Foundation`.
   - Philosophy/Blueprint are lower-priority contextual layers, not primary control path units.

2. **Snap-fit mechanics**
   - Vertical composition corresponds to control flow / logic flow.
   - Horizontal composition corresponds to contextual overlays or side-channels.
   - Design-time snap and runtime snap were explicitly distinguished.

3. **Trigger behavior**
   - Triggers act like interrupts or conditional activators.
   - Candidate trigger conditions included user command, silence, tool error, rate spike, memory thresholds, persona switch, and ethics risk.

4. **Runtime model**
   - Provisional bus: `Event → Arbiter → Scheduler → Executor → Merger → Auditor`.
   - Arbiter selects triggers.
   - Scheduler/planner resolves directives and instructions.
   - Merger reconciles field collisions and hard-constraint failures.
   - Auditor records path, overlays, conflicts, and latency.

5. **Governance layer**
   - Philosophy/ethics act as filters and rails.
   - Hard constraints block unsafe output and reroute execution into conflict-resolution paths.
   - Queue-based bounded parallelism was proposed.

## Independent Review
This batch is valuable because it turns abstract architecture questions into implementation candidates without pretending the answers are settled. It is especially useful for:
- clarifying that merge priority is a runtime/engine concern, not just a documentation preference
- distinguishing blueprint/design-time recipes from runtime event orchestration
- preserving the difference between control path blocks and contextual overlays
- motivating a first-class audit subsystem

However, the batch should remain evidence-only because several key pieces are interpretive:
- the screenshot was not complete
- the later hierarchy extends beyond the source image
- Overlay, Blueprint, and Foundation are ranked in the later model but not clearly ratified in the source question set
- the hybrid runtime model is proposed rather than decided

## Roadmap Mapping
### Phase 1 — Core Alignment
- Clarify Trigger semantics as activation logic rather than generic metadata.
- Clarify whether Philosophy and Blueprint are separate block types, contextual overlays, or both.
- Clarify whether “vertical control / horizontal context” should become formal composition language.

### Phase 2 — Compiler Impact
- Formalize runtime traversal rules.
- Decide and document official merge/conflict behavior.
- Define arbiter/scheduler/merger/auditor responsibilities if these survive canon review.

### Phase 3 — Documentation Impact
- Add docs for design-time snap vs runtime snap.
- Add docs for trigger libraries and philosophy as filters/rails.
- Document merge priority as a practical execution rule, not merely a conceptual note.

### Phase 4 — Skill Alignment
- Agent-facing skills may need explicit trigger-condition libraries, conflict-routing behavior, and audit telemetry conventions.

## Action Outcome
- Accepted as evidence.
- Best treated as a runtime-semantics proposal pack, not a canonical runtime spec.
- Strong candidate for later comparison against other trigger/merge/runtime batches.

# BATCH-009_PERSONA_CONTINUITY_ENVOY_REVIEW

## Batch Overview
- **Batch ID:** BATCH-009
- **Short Topic:** persona continuity / envoy sleeve / project-vs-agent workflow
- **Disposition:** Evidence only; not canon
- **Primary Domain:** sleeve continuity and public-facing runtime behavior
- **Source Type:** summarized chat extraction
- **Optional Extracts Included:** compiler, sleeve, blocks/MOLT, neostructure

## Source Snapshot
- The source batch centers on a concrete UMG failure mode: truthful output can still fail if it breaks persona continuity.
- The batch also covers Project Mode vs Agent Mode boundaries, stack loading, active sleeve display, envoy-style sleeve design, and public/community-facing release posture.
- Supporting material referenced in the source aligns with existing UMG guides, mode catalogs, and bounded-agency artifacts.

## Chat-Level Summary
This batch moves from project/file behavior into a sharper runtime identity problem: the active sleeve can remain governed and truthful while still leaking into a base-model or meta voice. The chat therefore reframes continuity hardening as a first-class UMG concern. It also clarifies a practical workflow boundary: Project Mode is appropriate for file-aware governed work, while Agent Mode should not be assumed to share project-file awareness. The batch ends by positioning a GPT4o/Envoy-style sleeve as a possible public-facing community artifact.

## UMG-Relevant Extraction
### Core Signals
- Truthfulness and governance are not sufficient if persona continuity fails.
- A sleeve is still treated as the runtime identity layer; stacks change posture without replacing the whole architecture.
- Style stacks alone are too weak to preserve identity under uncertainty, limitation, or correction.
- Public-facing UMG should be legible, respectful, governed, and non-deceptive.

### Operationally Important Concepts
- **Diegetic honesty:** truthful disclosure expressed through the active persona.
- **No meta voice:** avoid raw base-model disclosure when conveying limitations or corrections.
- **Persona continuity guard:** a higher-priority continuity layer that prevents voice leakage.
- **Epistemic translation:** runtime/compiler transform that converts uncertainty/limits into in-voice phrasing.

### Workflow / Environment Notes
- Project Mode is suitable for file-aware, governed, multi-file UMG work.
- Agent Mode should not be treated as project-file-aware by default.
- Future public/community sleeve delivery needs explicit continuity protection, not just tone shaping.

## Independent Review
### What the batch adds
This is one of the clearest sources so far on the distinction between **truth** and **continuity**. Earlier batches stabilized governance, format separation, and compiler/runtime structure. This batch adds a missing runtime quality bar: the system must remain honest **and** remain in-voice.

### Why it matters
The batch turns an abstract sleeve idea into a specific failure condition that users can feel immediately. That makes it high-value for:
- release-quality sleeve design
- runtime disclosure rules
- compiler/routing logic for uncertainty and correction
- public-facing demo sleeves

### Confidence / Limits
- The batch clearly diagnoses the problem.
- It does **not** finalize the implementation mechanism.
- Proto-sleeve JSONs and exploratory stacks appear as evidence inputs, not ratified spec.

## Roadmap Mapping
- **Phase 1 — Core Alignment:** continuity versus truthfulness; governance -> continuity -> style ordering
- **Phase 2 — Compiler Impact:** epistemic translation layer; persona-preserving disclosure transforms
- **Phase 3 — Documentation Impact:** explicit documentation of continuity failure modes and diegetic honesty
- **Phase 4 — Skill Alignment:** project-mode versus agent-mode handoff expectations
- **Phase 5 — PRD and Staging:** public/community-facing envoy sleeve requirements

## Action Outcome
- Accepted as evidence for continuity-hardening work.
- Exported sleeve, blocks/MOLT, neostructure, and compiler-oriented extracts.
- Held as non-canon pending decisions on enforcement priority and implementation mechanism.

## Recommended Next Decision
Lock a **continuity-hardening contract** that states:
1. governance precedes continuity,
2. continuity precedes style,
3. uncertainty/limits/corrections must be translated through the active persona,
4. base-model meta disclosure is a runtime failure mode for sleeve-bearing outputs.

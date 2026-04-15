# BATCH-022 — Initialisation / Base Interaction Review

## Batch Overview
- **Batch ID:** BATCH-022
- **Short Topic:** Initialization / Base Interaction
- **Source Type:** single compact chat summary
- **Stage:** Stage 1 intake only
- **Evidence Status:** non-canon
- **General Disposition:** useful as a baseline runtime-startup example rather than as deep doctrine

## Source Snapshot
- The source describes a minimal greeting exchange where the user says only “hi.”
- The assistant responds with a full UMG envelope instead of an ordinary greeting.
- The runtime exposes:
  - active sleeve
  - lightweight startup stacks
  - runtime action flags
  - MOLT interpretation
  - bounded startup posture
- The source therefore functions as a clean initialization specimen.

## Chat-Level Summary
This batch is a small but coherent example of how a UMG-configured conversation begins. It shows a default `Base Interaction` posture under `SLV.POE_UMG.MAIN.v1`, exposes a lightweight startup stack set, keeps external action and memory mutation off, and routes even a greeting through a visible MOLT-style reasoning surface. Its value is mostly architectural and operational: it shows startup behavior, not mature theory expansion.

## UMG-Relevant Extraction

### 1. Startup runtime posture
- Base interaction is treated as an explicit runtime mode rather than casual unstructured chat.
- The startup posture is bounded and non-mutating.
- The session starts ready for routing, not for autonomous execution.

### 2. Sleeve visibility
- Active sleeve is made visible immediately.
- The startup sleeve is `SLV.POE_UMG.MAIN.v1`.
- Sleeve identity is surfaced before deeper work begins.

### 3. Startup NeoStack pattern
- The startup stack set is lightweight and intake-oriented:
  - `NSTK.CONTEXT.MAPPING.v1`
  - `NSTK.SIMPLIFICATION.ENGINE.v1`
  - `NSTK.OUTCOME.FOCUS.v1`
  - `NSTK.OUTPUT.ENVELOPE.v1`
- This suggests a default conversation-opening posture built for routing, clarification, and clean response shaping.

### 4. MOLT routing at greeting time
- Even the greeting is structurally interpreted.
- Trigger is explicitly identified as the user greeting.
- The runtime treats simple input as routable through a MOLT skeleton rather than as architecture-free small talk.

### 5. Envelope behavior
- The startup example uses a full visible envelope:
  - Active Stack
  - Envoy Intuition
  - Current Context / MOLT Map
  - main prose
  - Metadata
- The prose remains lightweight while the structural frame remains explicit.

### 6. Bounded startup behavior
- Runtime flags explicitly keep:
  - execution bounded
  - external action off
  - memory mutation off
- The system is available for further routing without taking external action by default.

## Independent Review
This is a low-volume batch but a high-clarity specimen. It does not advance deep semantics like merge, bundle, compiler internals, or governance law. Its real value is that it captures a default initialization contract. That matters because startup behavior often becomes implicit and undocumented. Here, startup is explicit, bounded, structured, and sleeve-visible.

The batch is especially useful for:
- documenting what “conversation start” means in UMG
- defining a default startup stack set
- clarifying that trivial inputs still pass through a routing/control layer
- showing how visible envelope + light prose can coexist

This batch should remain evidence, not canon, until the project explicitly decides whether this exact startup posture is the intended baseline across hosts.

## Roadmap Mapping
- **Phase 1 — Core Alignment:** useful for defining baseline startup semantics and sleeve visibility
- **Phase 2 — Compiler Impact:** minor but relevant for startup defaults and runtime flag exposure
- **Phase 3 — Documentation Impact:** strong relevance for initialization docs and examples
- **Phase 4 — Skill Alignment:** relevant if startup routing becomes a reusable skill behavior
- **Phase 5 — PRD / Staging:** modest relevance as a default session-start pattern

## Action Outcome
- Batch accepted as evidence.
- Best use is as:
  - startup example
  - initialization behavior reference
  - bounded default posture example
- No canon promotion is implied.

## Recommended Next Decision
Decide whether UMG should standardize a **default initialization contract** with:
- one default base-interaction sleeve
- one lightweight startup stack set
- explicit startup runtime flags
- a documented rule for how minimal inputs get routed

# BATCH-100_UMG_MVP_PLAN_REVIEW

## Batch Overview
- **Batch ID:** BATCH-100
- **Short Topic:** UMG MVP Plan
- **Source Type:** Derived extraction / handoff note, not raw transcript
- **Review Status:** REVIEWED
- **Disposition:** ACCEPT_AS_EVIDENCE
- **Primary Domain:** MVP release planning, compiler/runtime deliverables, and business/governance strategy
- **Confidence Note:** This batch is unusually concrete on release planning and implementation targets, but provenance remains limited because it compresses a prior chat into a summarized extraction rather than preserving the raw exchange.

## Source Snapshot
- Source title: `100 UMG MVP Plan`
- Source character: summarized extraction of a prior conversation
- Main themes surfaced by source:
  - 8-week MVP delivery plan and 12-month financial projection
  - CompileMOLT, MOLT-Graph Runtime, and block JSON schema
  - open-core business model with Apache 2.0 + defensive IP strategy
  - starter block library, visual editor, and SaaS launch path
  - adoption funnel, valuation framing, and revenue streams
- Provenance caution:
  - the source mixes implementation planning, business strategy, and governance proposals without independently verifying which items were already built versus still proposed.

## Chat-Level Summary
This batch pushes UMG from high-level architecture into concrete MVP execution. Its strongest signal is the coupling of an explicit build path—CompileMOLT, deterministic graph runtime, persistence schemas, starter blocks, visual editor, and deployment pipeline—with a parallel business and governance model covering open-core licensing, defensive patent posture, trademarks, and monetization. The source is especially useful because it does not treat release planning as separate from semantics: the block JSON schema, Cantocore-to-JSON normalization path, and graph-execution assumptions are all tied directly to the first public release plan. It also pressures downstream PRD work by supplying financial projections, KPI-like growth assumptions, and release-stage adoption logic.

## UMG-Relevant Extraction
### Core semantics
- Block JSON schema is treated as a core semantic surface, not just implementation detail.
- CompileMOLT is described as converting Cantocore into normalized JSON.
- MOLT-Graph Runtime is described as deterministic graph execution with memo caching.
- UMG is positioned as a “mind abstraction” layer rather than only an app or prompt workflow.

### MOLT / block signal
- Explicit block types are enumerated:
  - Primary
  - Subject
  - Instruction
  - Merge
  - Overlay
- A starter library of named blocks is reported, including:
  - `Alignment.Primer.v1`
  - `Philosophy.LoveLogic.v1`
  - `Subject.ArtOfWar.v1`
- The schema excerpt includes:
  - `id`
  - `type`
  - `cantocore`
  - `version`
  - `inputs`
  - `outputs`
  - `metadata`

### Runtime / compiler signal
- Deliverables explicitly include:
  - CompileMOLT (TypeScript)
  - MOLT-Graph Runtime
  - Qdrant vector layer
  - persistence schemas for `blocks`, `stacks`, and `versions`
- Execution is described as deterministic and memo-cached.
- Acceptance-test style compiler/runtime work is implied.
- Spec v0.1 is reported as the document meant to lock schema and pipeline contract.

### Stack / editor / architecture signal
- Visual editor is described as drag-and-drop assembly of 5-block stacks.
- Real-time Cantocore preview and WebSocket hot reload are reported as editor/runtime behaviors.
- Starter blocks, stack assembly, and runtime graph execution together imply a concrete first NeoStack/NeoBlock tooling surface.
- The visual editor pressures a user-facing representation of stack/graph structure.

### Governance / control signal
- Governance is framed through Apache 2.0 OSS core plus a provisional patent and proposed Patent Non-Assertion Pledge.
- Trademark filing for UMG and MOLT is recommended but not started.
- Dual licensing for add-ons is described as proposed, not selected.
- This batch links long-term governance directly to release and fork strategy.

### PRD / release signal
- The chat describes an 8-week MVP delivery path and a staged rollout to SaaS launch.
- 12-month financial projections, valuation scenarios, and adoption funnel logic are reported.
- CI/CD, deployment, and recurring sync rhythm are included as operational staging assumptions.
- Release planning is tied to showcase demos and integration-ready experiences.

## Independent Review
This batch is one of the clearest Stage 1 packets for **turning UMG into a release program** rather than only refining its abstract architecture. The strongest extraction is the triad of **schema**, **compiler/runtime**, and **MVP staging**. Together these provide unusually concrete evidence for what a first public implementation would actually need.

The most valuable compiler signal is the explicit pairing of **CompileMOLT** with a **deterministic memo-cached graph runtime**. That pairing pressures the project to decide whether UMG’s first execution surface is fundamentally sequential, graph-based, or hybrid. The mention of persistence schemas and vector retrieval strengthens that implementation signal further.

A second high-value signal is the **business/governance integration**. The source does not treat OSS licensing, patents, and trademark posture as separate legal add-ons; it treats them as part of how UMG should survive forks, monetize responsibly, and preserve ecosystem coherence. That is strategically important, but still requires later legal validation.

The main caution is that projections, valuation, moat language, and some product assumptions are inherently speculative. Stage 1 should preserve them as structured evidence for PRD and release planning, not as validated market fact.

## Roadmap Mapping
### PHASE_1_CORE_ALIGNMENT
- pressures definition of:
  - block schema baseline
  - Overlay as a role/type
  - first-release semantic contract for CompileMOLT inputs/outputs

### PHASE_2_COMPILER_IMPACT
- pressures need for:
  - normalized Cantocore-to-JSON compilation
  - deterministic graph execution
  - memo caching behavior
  - persistence models for blocks/stacks/versions
  - runtime acceptance tests

### PHASE_3_DOCUMENTATION_IMPACT
- pressures need for:
  - Spec v0.1 schema documentation
  - CompileMOLT pipeline documentation
  - starter block documentation
  - public explanation of OSS/IP posture

### PHASE_4_SKILL_ALIGNMENT
- suggests:
  - showcase integration patterns
  - starter demo workflows
  - runtime-preview/editor behaviors that influence skill packaging and examples

### PHASE_5_PRD_AND_STAGING
- strongly pressures:
  - MVP scope locks
  - phase gates
  - KPI and revenue assumptions
  - launch, hosting, CI/CD, and monetization planning

## Action Outcome
- **Disposition chosen:** ACCEPT_AS_EVIDENCE
- **Why:** the batch is unusually concrete and strategically important, but it remains a derived summary that mixes implementation planning, business modeling, governance proposals, and speculative growth assumptions.
- **Optional extracts justified:**
  - `COMPILER_EXTRACT` because the source contains explicit schema, compilation, graph-runtime, caching, persistence, and test pressure.
  - `BLOCKS_MOLT_EXTRACT` because the batch contributes schema fields, enumerated types, and starter block-library signal.
  - `NEOSTRUCTURE_EXTRACT` because the source includes stack/graph/editor assembly behavior and concrete first-release structure assumptions.

## Recommended Next Decision
Decide whether the Block JSON schema plus CompileMOLT → MOLT-Graph Runtime pipeline should become the working implementation baseline for Spec v0.1, or remain provisional until reconciled with earlier evidence on role taxonomy, stack ordering, and overlay/merge semantics.

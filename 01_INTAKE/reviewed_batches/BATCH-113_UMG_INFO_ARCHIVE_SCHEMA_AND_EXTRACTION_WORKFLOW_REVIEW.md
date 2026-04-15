# BATCH-113 — UMG Info Archive Schema and Extraction Workflow Review

## Batch Overview
- **Batch ID:** BATCH-113
- **Source Type:** Derived extraction / handoff note
- **Review Status:** REVIEWED
- **Disposition:** ACCEPT_AS_EVIDENCE
- **Primary Domain:** archival schema, transcript extraction, and conflict-detection workflow
- **Canon Status:** Evidence only, not canon

## Source Snapshot
- The source summarizes a chat that created a dedicated **UMG Info Archive** context for gathering comparable information from UMG conversations over time.
- The chat moved from a broad extraction wish-list into a typed archive schema, required versus optional fields, ingestion stages, conflict detection, and report/PDF rendering ideas.
- It also explored whether transcript ingestion could be routed through an agent or workflow to produce organized outputs.
- The source is not a raw transcript. It is a structured summary and should be treated as evidence with preserved uncertainty.

## Chat-Level Summary
This batch contributes an archival and operational layer around UMG rather than altering core UMG doctrine directly. Its strongest signal is a proposed **archive object model** that stores chats, turns, artifacts, and conflicts in typed, versionable form. The batch also proposes a deterministic ingestion pipeline—normalize, segment, extract, version, index, conflict-check, persist—and a transcript-to-structured-report path that could make UMG discussion history more parsable, comparable, auditable, and reusable across chats.

## UMG-Relevant Extraction
### Core signal
- UMG conversation history should be turned into typed artifacts rather than remaining only as prose.
- The archive is meant to support:
  - diffing cognition across time
  - conflict detection before execution
  - versioned comparison between chats
  - traceable evolution of UMG itself

### Archive-facing object model
- Proposed archive objects include:
  - archive metadata
  - chats
  - turns
  - artifacts
  - conflicts
- Proposed artifact classes include:
  - definitions
  - rules
  - sleeves
  - blocks / NeoBlocks
  - JSON/code
  - analyses
  - assumptions
  - terminology drift
  - authority decisions
  - constraint violations

### Deterministic workflow pressure
- Ingestion is proposed as deterministic and staged, not free-form reinterpretation.
- Ambiguous material is preserved as **candidate** rather than discarded or silently canonized.
- Conflict logic is proposed as explicit, typed, severity-ranked, and evidence-backed.

### Output/render value
- The chat separates:
  - transcript collection
  - artifact extraction
  - conflict detection
  - final report/PDF rendering
- That creates a clear raw-chat → normalized archive → rendered output pipeline.

## Independent Review
### What appears strong
- This batch is unusually strong as **archive infrastructure** for the project.
- It gives a practical mechanism for turning prior chat history into:
  - typed evidence
  - comparable records
  - explicit conflicts
  - structured report outputs
- It fits the control-room need to keep evidence separate from canon while still making it queryable and reusable.

### What remains unresolved
- It is not settled whether this archive schema should become:
  - canonical project infrastructure,
  - or remain a working archive tool.
- Trigger, priority, merge, and bundle are named as extraction targets but are not semantically developed here.
- The runtime-style sleeve JSON appearing in the chat is representational but not clearly ratified as canon.
- Conflict auto-resolution methods are proposed, but acceptance criteria for automation versus manual review are not finalized.
- No final implementation environment is selected for the external agent/workflow path.

### Provenance caution
- This is a summarized extraction, not a raw transcript.
- Much of the archive schema and workflow logic appears assistant-proposed in response to the user’s request and should not be silently upgraded to canon.

## Roadmap Mapping
### Phases touched
- **PHASE_1_CORE_ALIGNMENT**
  - adds archive categories for definitions, rules, conflicts, sleeves, and blocks
  - supports cross-chat comparison without canon promotion
- **PHASE_2_COMPILER_IMPACT**
  - proposes deterministic ingestion and conflict-detection pipeline
  - suggests typed artifact emission, indexing, and persistence
- **PHASE_3_DOCUMENTATION_IMPACT**
  - provides archive taxonomy, field structure, payload templates, and report structure
- **PHASE_4_SKILL_ALIGNMENT**
  - proposes staged extractor / validator / conflict / publisher workflow
- **PHASE_5_PRD_AND_STAGING**
  - suggests transcript-to-structured-report packaging path

## Action Outcome
- Accepted as evidence, not canon.
- Optional extracts justified:
  - **COMPILER_EXTRACT** for ingestion pipeline, conflict pass, and persistence logic
  - **BLOCKS_MOLT_EXTRACT** for block/sleeve payload structure and MOLT-role serialization
  - **CONTRADICTION_FLAGS** for schema-ratification, automation-boundary, and canon-vs-tool tensions
- No canon promotion performed.

## Recommended Next Decision
Decide whether the **UMG Info Archive** should be treated as:
1. a Stage 1 evidence-management tool only,
2. a control-room infrastructure layer with stable object model,
3. or an eventual canonical subsystem for transcript-derived UMG knowledge management.

Until that is resolved, this batch should remain evidence supporting archive design and workflow planning rather than canon.

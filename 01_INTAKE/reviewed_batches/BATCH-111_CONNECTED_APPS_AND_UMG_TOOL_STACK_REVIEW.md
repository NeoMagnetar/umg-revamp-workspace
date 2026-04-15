# BATCH-111 — Connected Apps and UMG Tool Stack Review

## Batch Overview
- **Batch ID:** BATCH-111
- **Source type:** Derived extraction / handoff note
- **Review status:** REVIEWED
- **Disposition:** ACCEPT_AS_EVIDENCE
- **Primary domain:** tool-stack orchestration, compiler/runtime enablement workflow, and corpus-to-system transition
- **Canon status:** Not canonized
- **Reason for intake:** The source concentrates practical workflow structure for turning scattered UMG docs/chats into a more organized, human-in-the-loop system spanning Drive, GitHub, structured registry work, and compiler/runtime planning.

## Source Snapshot
- The source summarizes a conversation about what connected Google Drive can do inside ChatGPT, what other apps are available, and how they could be combined into a UMG-oriented workflow.
- It includes a Drive search pass that surfaced UMG-related documents and snippets.
- It proposes a staged app/tool workflow rather than a finalized architecture.
- The source is not a raw transcript. It is an extracted summary and must therefore be treated as evidence with preserved uncertainty.

## Chat-Level Summary
This batch is a practical enablement packet rather than a pure theory packet. It identifies a real tool environment around UMG, surfaces an existing Drive corpus, and proposes a role split in which Drive holds narrative/canonical material, GitHub holds code, structured registries hold operational truth, design/deploy apps handle front-end legibility, and ChatGPT acts as the orchestration bridge. The source also contributes compiler-adjacent signal from a runtime warning document, especially around trace, governance, trigger use, priority conflict resolution, bundle hygiene, and merge diagnostics.

## UMG-Relevant Extraction

### Corpus and storage signal
- The source surfaced a small UMG corpus in Drive spanning theory, architecture, runtime warnings, and implementation scaffolding.
- Those materials are treated as evidence inputs for later canonization, not as already-final canon.
- The chat frames the next step as moving from scattered docs/chats into explicit storage, structured rules, compiler work, and front-end presentation.

### MOLT / cognition-role signal
- A surfaced framework snippet described:
  - **Primary** as base abilities / ethical compass
  - **Merge** as contextual adaptation or injected information
  - **Blueprint** as high-level plan, tone, philosophy, or approach
- A later diagram proposal listed:
  - Trigger → Directive → Instruction → Subject → Primary → Philosophy → Blueprint → Output
- The diagrammed flow should be treated as explanatory workflow aid, not ratified canon from this chat.

### Governance / trace / warning signal
- A surfaced runtime warning doc included warning/error vocabulary around:
  - unused triggers
  - skipped governance rules
  - soft governance overrides
  - directive conflict resolution
  - instruction conflict resolution
  - redundant bundles
  - unused bundle/merge segments
  - multiple primary candidates
- A surfaced snippet also included trace/compile structures such as `TraceEvent` and `CompileResult`.
- Governance and diagnostics therefore appear here as compiler/runtime documentation signal.

### Tool-stack workflow signal
- The chat proposed a human-in-the-loop orchestration pattern:
  - Google Drive = canonical narrative memory / source corpus
  - structured registry layer = operational truth / ledger
  - GitHub = compiler/code/repo
  - design/deploy apps = diagrams, front-end explanation, delivery
  - ChatGPT = orchestration/conductor layer
- The source repeatedly stresses that apps do not directly merge with each other; ChatGPT is the bridge.

### Compiler / rollout signal
- Proposed future compiler work includes:
  - parser
  - merge engine
  - governance resolver
  - trace generator
  - compile / validate / trace endpoints for a future MCP layer
- Proposed phases include:
  1. canon extraction from Drive/chats
  2. structured canon registry
  3. diagrams + IP
  4. compiler + MCP
  5. human-in-the-loop operating workflow

## Independent Review
This batch is high-value evidence for operationalization and staging rather than for final semantics. Its most useful contribution is the practical division of responsibilities across tools plus the surfaced runtime/governance warning language from existing documents. It helps the control project distinguish between human-readable canon, structured operational truth, compiler/runtime work, and presentation/deployment layers.

This batch should not be over-promoted. Several proposed structures remain provisional, including registry schemas, MCP endpoints, tool splits, and explanatory MOLT flow ordering. The Drive results are document-based and useful, but they are not equivalent to confirmed canon folders or canonical decisions.

## Roadmap Mapping
- **PHASE_1_CORE_ALIGNMENT**
  - evidence intake from existing Drive corpus
  - dedup/canonization pressure from multiple copies / overlapping docs
- **PHASE_2_COMPILER_IMPACT**
  - warning/error vocabulary
  - trace schema pressure
  - parse → validate → assemble → emit runtime + trace pipeline proposal
- **PHASE_3_DOCUMENTATION_IMPACT**
  - glossary / governance / RuntimeSpec / Trace / sleeve schema documentation proposals
  - separation of narrative canon from structured operational truth
- **PHASE_4_SKILL_ALIGNMENT**
  - ChatGPT-as-orchestrator workflow
  - phone + laptop hybrid work pattern
  - human-in-the-loop executor/governor split
- **PHASE_5_PRD_AND_STAGING**
  - staged build path from canon extraction to compiler/MCP to front-end/deployment
  - tool-role split for shipping legible artifacts

## Action Outcome
- Accepted as evidence.
- Optional extracts added for:
  - compiler/runtime warning and trace impact
  - blocks/MOLT/runtime warning semantics
  - contradiction flags around tool-role claims and provisional structure
- No canon promotion performed.
- No Airtable/app-stack canonization performed beyond what the source supports.

## Recommended Next Decision
Freeze a control-room intake memo on tool-role separation that:
1. distinguishes corpus storage, structured registry, compiler repo, and front-end delivery,
2. extracts the runtime warning vocabulary into a tracked diagnostics schema candidate,
3. treats all registry/MCP/app-stack proposals as provisional until explicitly validated in the workspace.

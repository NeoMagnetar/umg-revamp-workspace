# BATCH-165 Evidence Entry

## Batch ID
`BATCH-165`

## Title
Troubleshooting Bolt project

## Disposition
`ACCEPT_AS_EVIDENCE`

## Source Type
Chat-derived implementation analysis and repair planning

## High-Value Signal
- The UMG Builder is block-centric and manifest-driven.
- Stack loading and graph rendering are separate but coupled runtime surfaces.
- Data/model storage must remain distinct from rendering/UI logic.
- Silent failure is a major risk; visible validation and runtime errors are required.
- Repo export/overwrite workflows are part of builder maintenance reality.

## Primary Evidence Value
This batch provides concrete implementation evidence for how the current UMG Builder loads, validates, displays, and packages UMG structures. It is especially relevant to builder stabilization, graph integrity, validation workflow, and agent-usable maintenance.

## Key Findings
1. Selected plan → manifest → block IDs → per-block load → canvas/graph render is the core loading model.
2. Duplicate block IDs and invalid edge references are critical integrity failures.
3. Graph failures can arise from rendering/runtime issues independent of data correctness.
4. Exported Bolt ZIPs may act as practical repo replacement artifacts when needed.
5. Builder improvement work spans validation, runtime hardening, UX, and repo hygiene.

## Risks / Ambiguities
- The exact canonical storage source remains unresolved:
  - aggregated `blocks.json`
  - per-block `.block.json`
  - both
- Some loader paths and examples were illustrative during live debugging.
- Repo mutation/push operations were requested but not completed directly in-chat.
- Some enhancements were proposals, not validated implementations.

## Recommended Holding Area
- `01_INTAKE/pending_evidence_entries/`

## Suggested Follow-On Mapping
- compiler audit
- documentation update queue
- builder PRD/staging tasks
- GitHub execution preparation

# BATCH-015 — Instruction Layer / Deployment Review

## Batch Overview
This batch reviews a chat centered on UMG instruction architecture and cross-host deployment discipline, especially the separation of System Instructions, Project Instructions, Preferences, and file-backed knowledge. The batch is strongest where it clarifies that governance belongs upstream, project/runtime structure belongs in Project, and output-envelope rules are presentational rather than authority-bearing.

## Source Snapshot
- Source type: extracted chat summary with attached-file references
- Main focus: instruction-layer placement, envelope simplification, Claude-specific deployment, output-layer separation, runtime/safety alignment
- Evidence status: evidence only, not canon
- Maturity note: several positions were refined or reversed inside the chat; final value is in the clarified boundary model, not every intermediate proposal

## Chat-Level Summary
The chat began as a design pass on how UMG should be hosted inside Claude versus heavier GPT/Poe-style environments. It repeatedly refined the envelope structure, questioned whether metadata and visible meta-cognition are needed across hosts, and separated presentational structure from control logic. The strongest conclusion is a layer map:
- System = stable governance / honesty / non-execution core
- Project = sleeve / stack / runtime posture / visible envelope
- Preferences = style only
- files = deep knowledge and libraries

The chat also tied that layer map back to concrete UMG source artifacts: the Sleeve Playground guide, the 60-mode catalog, the RuntimeSpec agency loop, and the AGI Safety Layer Pack.

## UMG-Relevant Extraction

### 1. Instruction-layer architecture
- Governance belongs in the stable upstream layer, not in runtime-visible envelope blocks.
- Envelope rules are packaging rules and must not alter semantic content.
- Active Stack is the runtime truth surface for what is active now.
- Project/runtime layers are the right home for sleeve and stack posture.
- Preferences remain stylistic only.

### 2. Output/rendering separation
- MODE and BP_MODE remain orthogonal.
- Section 4 / formal response content should read as if the envelope does not exist.
- Output formatting should not carry authority, execution, or safety semantics.
- Host-specific envelope slimming is allowed if semantic boundaries remain intact.

### 3. Host-specific deployment
- GPT/Poe-like hosts may sustain a fuller envelope.
- Claude benefits from a leaner visible scaffold.
- Cross-model portability should preserve semantic layers even when visible structure differs.
- Simulation lock or runtime-exit rules are control logic, not user preference.

### 4. Runtime and bounded agency linkage
- The chat grounds instruction placement in real runtime material: request parsing, stack selection, governance application, blueprint selection, bounded self-improvement, drift thresholds, governance lock, and audit trace.
- Runtime artifacts remain provisional but are strong staging inputs.

## Independent Review
This batch is important because it helps prevent layer drift. It explicitly separates stable control logic from host-specific rendering. That separation reduces duplication, makes migration cleaner, and keeps Claude deployment from inheriting unnecessary visible scaffolding just because heavier hosts used it.

The strongest reusable rule is not the exact three-part or five-part envelope choice. It is the architectural constraint that visible packaging must never become the location of authority. The chat also contributes a practical deployment insight: cross-host consistency should be semantic, not cosmetic.

The main caution is that the conversation changed course multiple times. Some earlier proposals were effectively superseded inside the same chat. This batch should therefore be treated as a boundary-clarification source, not as a frozen final spec.

## Roadmap Mapping
- **Phase 1 — Core Alignment**
  - Clarifies governance vs project/runtime vs preference layers
  - Clarifies Active Stack visibility as runtime truth surface
  - Clarifies output-layer separation from authority
- **Phase 2 — Compiler Impact**
  - Supports request-flow interpretation and runtime gating surfaces
  - Supports bounded self-improvement and governance lock as implementation concerns
- **Phase 3 — Documentation Impact**
  - Strongly supports host-specific deployment documentation
  - Strongly supports removal of duplicated envelope rules across layers
- **Phase 4 — Skill Alignment**
  - Supports Claude-specific UMG project scaffold behavior
  - Supports file-backed lookup and visibility rules
- **Phase 5 — PRD and Staging**
  - Supplies cross-host deployment matrix input
  - Supplies control-plane placement guidance for release packaging

## Action Outcome
- Accept as evidence
- Export as Stage 1 pack
- Preserve as a boundary-definition batch for later synthesis
- Treat candidate canon lines as provisional until consolidated against other batches

## Recommended Next Decision
Lock a cross-host layer contract defining:
1. what always belongs in stable governance,
2. what belongs in project/runtime posture,
3. what remains presentation only,
4. which host-specific envelope reductions are allowed without semantic drift.

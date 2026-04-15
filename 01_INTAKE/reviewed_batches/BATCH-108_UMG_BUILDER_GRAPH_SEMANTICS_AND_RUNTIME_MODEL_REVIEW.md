# BATCH-108 — UMG Builder Graph Semantics and Runtime Model Review

## Batch Overview
- **Batch ID:** BATCH-108
- **Source type:** Derived extraction / handoff note
- **Review status:** REVIEWED
- **Disposition:** ACCEPT_AS_EVIDENCE
- **Primary domain:** Builder graph semantics, runtime interaction model, and stack behavior
- **Confidence note:** High value for builder/runtime semantics; lower provenance than raw transcript because the source is a summarized extraction rather than direct conversation text.

## Source Snapshot
- Focused on stabilizing the UMG Builder web app after a misaligned early build.
- Re-centered the app on Universal Modular Generation rather than unrelated branding drift.
- Moved from general repo/scaffold concerns into concrete builder semantics:
  - graph canvas behavior
  - Primary-root hierarchy
  - stack priority
  - merge/overlay logic
  - manifest/block loading
  - JSON editing
  - category organization by plan type
- Repeatedly favored minimal, Bolt-readable implementation guidance over broad rewrites.

## Chat-Level Summary
This batch translates UMG into a practical builder interface and runtime interaction model. The central semantic move is that the builder must preserve UMG hierarchy even when using a graph UI: the user always starts with a Primary block, nothing may sit above Primary, vertical placement represents stack depth/priority, and horizontal placement represents overlay/merge behavior. The conversation also established implementation pressure around a manifest-driven runtime, graph conversion utilities, snap logic, merge evaluation, JSON editing, and a future terminal-like panel. The app is framed as a thought IDE / mind IDE rather than a generic flowchart editor.

## UMG-Relevant Extraction

### 1. Core semantics
- UMG Builder is for structured logic, plans, and AI cognition, not a generic block toy.
- The app should explicitly align with **Universal Modular Generation** branding and semantics.
- Three top-level creation modes were treated as central:
  - business plan
  - web app
  - chatbot

### 2. MOLT and builder structure
- Primary is the mandatory root / starting block.
- Other roles attach around it through vertical stack growth or horizontal overlay/merge placement.
- The batch used a wizard framing including:
  - Primary
  - Subject
  - Instruction
  - Philosophy
  - Blueprint
  - Directive
  - Trigger
  - Deployment
  - Off
- Structural behavior mattered more than color or decoration:
  - Primary starts
  - vertical means hierarchy
  - horizontal means overlay/merge

### 3. Runtime / builder behavior
- Manifest + block loading should drive graph rendering.
- Graph UI freedom must be subordinate to UMG logic constraints.
- Proposed runtime-adjacent files:
  - `GraphCanvas.tsx`
  - `flowUtils.ts`
  - `snapLogic.ts`
  - `mergeEngine.ts`
  - `DockLayout.tsx`
  - `BlockNode.tsx`
  - `StackColumnGuide.tsx`
  - `ZoomControls.tsx`
- Proposed functions included:
  - `canMerge(target, incoming)`
  - `mergeBlocks(target, incoming)`

### 4. Stack semantics
- Nothing can go above Primary.
- Vertical drop updates stack priority and places the block below a parent/root.
- Horizontal drop attempts overlay/merge when allowed.
- Save/load should preserve:
  - stack order
  - grouping
  - relative placement semantics
- New blank-space drops may create a new stack group.

### 5. Editing and representation
- Blocks remain editable JSON units.
- JSON editor panel should remain first-class.
- Builder should feel like block-as-file / block-as-code, not just node-as-widget.
- Terminal-like UI was desired, but AI/runtime activation was intentionally deferred.

## Independent Review
This is one of the clearest builder-facing packets in the intake stream. Its strongest contribution is not a new theory of UMG but a practical semantics bridge between UMG stack logic and a graph-based editor. The source repeatedly protects UMG against dilution by generic graph tooling. The most durable signal is the Primary-root rule, followed by the vertical-versus-horizontal split and the insistence that graph freedom cannot override semantic structure.

The batch also contains unresolved or potentially unstable elements. `Deployment` appears inside the builder-facing wizard role set, but the broader intake stream has already raised discomfort with `Deployment` as a main MOLT role. Likewise, the exact interaction model for merge, undo-merge, save/export of merged state, and docking behavior remains provisional.

## Roadmap Mapping
- **Phase 1 — Core Alignment**
  - Confirms Primary-root semantics as a likely high-value alignment rule.
  - Reinforces distinction between stack hierarchy and overlay/merge behavior.
- **Phase 2 — Compiler Impact**
  - Strong impact on snap logic, merge logic, node conversion, and canvas serialization.
  - Supports explicit stackPriority handling and no-above-primary enforcement.
- **Phase 3 — Documentation Impact**
  - Good candidate language for builder spec and UI semantics.
  - Needs clarification on plan-type categories and role descriptions.
- **Phase 4 — Skill Alignment**
  - Relevant to builder-oriented skills and any skill that emits or edits block graph state.
- **Phase 5 — PRD and Staging**
  - Strong input for MVP stabilization sequence:
    - block loading
    - plan-type selection
    - graph canvas recovery
    - stack/merge UX refinement
    - defer AI hooks

## Action Outcome
- Accepted as evidence.
- Frozen as a Stage 1 pack.
- Optional extracts justified for:
  - compiler/runtime behavior
  - blocks/MOLT semantics
  - neostructure / graph-stack architecture
  - contradiction flags

## Recommended Next Decision
Decide whether **Primary-root enforcement + vertical stack / horizontal merge semantics** should be treated as the canonical builder interaction model, and resolve whether `Deployment` remains in any active builder-facing role taxonomy or is removed/recast.

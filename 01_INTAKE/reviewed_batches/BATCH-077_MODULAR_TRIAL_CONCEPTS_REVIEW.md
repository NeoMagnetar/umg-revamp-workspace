# BATCH-077 — Modular Trial Concepts — Review

## Batch Overview
- **Batch ID:** BATCH-077
- **Short Topic:** Modular Trial Concepts
- **Source Type:** derived handoff summary / extracted chat notes
- **Review Status:** REVIEWED
- **Disposition:** ACCEPT_AS_EVIDENCE
- **Primary Domain:** ui_runtime_composition
- **Evidence Strength:** medium-to-strong for implementation-facing semantics; not raw-transcript canon

## Source Snapshot
This batch captures a live UMG-facing product surface: a block-based "Command Center" / Block Manager UI with editable blocks, role assignment, code/skeleton views, and generated output. The chat centered on how selected blocks should combine to produce a concrete output example, then shifted toward system design and reformulation against the user's actual application stack.

## Chat-Level Summary
The source grounds UMG in an existing product environment rather than a whitepaper abstraction. It treats UMG as an editable, role-driven composition system where Primary, Merge, and Blueprint blocks each contribute differently to the final output. The strongest value here is implementation pressure: how role semantics, merge modes, editable instructions, and generation orchestration should work inside a React/TypeScript + Express/Node app. The key unresolved issue is deterministic behavior: the first generated example missed user intent, revealing that loose modular blending is insufficient without stricter runtime rules.

## UMG-Relevant Extraction

### Core Semantics
- UMG is treated as a modular output-construction system.
- Distinct blocks contribute distinct forms of influence to a final artifact.
- Primary, Merge, and Blueprint are the operative role set in this batch.
- The system aims to replace monolithic prompting with editable block controls.

### Role Behavior
- **Primary** = main intent / directive / target output ask.
- **Merge** = supporting content intended to be integrated.
- **Blueprint** = inspiration or style lens shaping render, not necessarily copied literally.
- The live UI already exposes role assignment and block activation.

### Implementation Surface
- Editable block cards imply practical block composition.
- The app already contains richer features than a toy demo:
  - Instruction System
  - Merge Controls
  - Skeleton Code Generation
  - Authentication Components
  - 3D UI Effects
- The runtime must fit the actual stack rather than a standalone example module.

### Runtime Signal
- Proposed logic: resolve active Primary, collect active Merge blocks, apply Blueprint influence.
- Immediate edit -> generate loop is an intended behavior.
- The app appears to support both text/content generation and code/skeleton generation.

### PRD / Product Signal
- The product is already beyond pure concept stage.
- Immediate priorities implied by the batch:
  - deterministic role-faithful generation
  - merge-mode semantics
  - transformation-stage rules
  - alignment of code proposals to the real repository/app stack

## Independent Review
This is a valuable Stage 1 batch because it anchors UMG semantics to a live control surface. It is strongest where it exposes semantic pressure from an implementation context: role names exist in UI, merge controls are advertised, and the user expects deterministic behavior from those controls. The source does **not** finalize runtime law, but it sharply narrows the space of acceptable future definitions.

The most important project value here is not new ontology. It is the demonstration that semantic ambiguity now causes visible product failure. "Binary" and "Art of War" each drift between content, style, and transformation concepts. That drift is not abstract; it produces wrong output. This makes the batch high-value for compiler/runtime formalization and documentation cleanup.

Because the source is a summary rather than a raw transcript, extraction remains evidence-only. None of the role or merge formulations here should be promoted to canon without cross-batch reconciliation.

## Roadmap Mapping

### PHASE_1_CORE_ALIGNMENT
- Clarifies practical meanings of Primary, Merge, and Blueprint in a live UI setting.
- Surfaces semantic ambiguity around transformation vs support vs style.

### PHASE_2_COMPILER_IMPACT
- Strong signal for deterministic resolution order.
- Strong signal for explicit transformation stages and merge-mode definitions.
- Raises frontend/backend execution-boundary questions.

### PHASE_3_DOCUMENTATION_IMPACT
- Supports documenting current live role taxonomy exactly as shown in UI.
- Supports distinguishing content-generation blocks from Skeleton Blocks.

### PHASE_4_SKILL_ALIGNMENT
- Supports block-edit -> immediate generation preview workflow.
- Relevant to any skill or agent surface that loads modular roles and renders output.

### PHASE_5_PRD_AND_STAGING
- Supports acceptance criteria for role-faithful generation.
- Supports staging work around editor fidelity, generation logic, and stack integration.

## Action Outcome
- Accept as evidence.
- Freeze as a Stage 1 pack.
- Route a compiler extract and blocks/MOLT extract because the source clearly supports both.
- Route contradiction flags because ambiguity pressure is explicit and materially relevant.

## Recommended Next Decision
Define whether role resolution should be:
1. **Primary -> Merge -> Blueprint**
2. **Primary -> transformation modifiers -> Merge -> Blueprint**
3. a mode-dependent resolver based on merge-control semantics (`blend`, `dominate`, `reference`)

Until that is decided, live UMG output behavior in the Block Manager will remain under-specified.

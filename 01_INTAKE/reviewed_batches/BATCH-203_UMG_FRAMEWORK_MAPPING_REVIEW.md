# BATCH-203 — UMG Framework Mapping — Review

## Batch Overview
- **Batch ID:** BATCH-203
- **Source Type:** derived architecture-and-workflow summary
- **Review Status:** REVIEWED
- **Disposition:** ACCEPT_AS_EVIDENCE
- **Primary Domain:** canon_storage_and_runtime_separation
- **Evidence Strength:** medium-high
- **Why it matters:** this batch defines a strong externalized model for UMG as a governed, file-based system with clear separation between canon, mapping, and runtime.

## Source Snapshot
- The source centers on how UMG should be stored, mapped, governed, and loaded outside chat.
- It compares tools and surfaces such as:
  - local files
  - Obsidian
  - ChatGPT Projects
  - Custom GPTs
  - Deep Research
- It repeatedly emphasizes that canon must live outside the model and that runtime should receive only selectively loaded fragments.
- It proposes object-level storage for blocks, sleeves, and stacks, plus a repeatable canonization workflow.
- The source is directional and architectural rather than a finalized schema or implemented compiler.

## Chat-Level Summary
This batch is a strong **canon storage and runtime separation** artifact. Its main contribution is the clear three-layer distinction:
- canon = source of truth
- mapping = visualization / structure workspace
- runtime = execution / reasoning surface

That distinction gives UMG a path out of prompt-only existence and into a governed, persistent, agent-usable system. The batch also pushes toward one-object-per-file storage, ID-based loading, structured metadata, and a three-pass canonization workflow.

## UMG-Relevant Extraction
### Core Semantics
- UMG is treated as a governed knowledge system rather than a prompt.
- Canon must exist outside the model.
- Chat is execution surface; filesystem is authoritative reality.
- Discrete objects are defined for:
  - sleeves
  - blocks
  - stacks

### Blocks / Sleeves / Stacks
- Blocks are stored as individual files.
- Sleeves are structured objects linking blocks and defining an execution lens.
- Stacks are implied as compositional layer or grouped load surface above blocks.
- Example IDs imply one-object-per-file conventions and versioned naming.

### Runtime / Loader Logic
- Runtime is defined as selective loading of sleeves and blocks into chat/agent surfaces.
- Loader behavior is conceptualized through:
  - explicit ID loading
  - no assumption about undeclared modules
  - marking missing definitions instead of inventing them
- The canonization workflow is proposed as:
  - inventory pass
  - normalization pass
  - backlog generation

### Governance / Control
- Strong external-canon principle:
  - never expose the full system unnecessarily
  - use selective runtime projection
- Optional integrity enhancement:
  - hash fields such as sha256
- Governance is tied to explicit loading, file-based control, and non-inventive handling of missing pieces.

### Documentation / Spec Direction
- Strong push toward:
  - YAML schema
  - stable naming conventions
  - versioned IDs
  - human-readable and machine-readable files
- Anchor docs proposed:
  - schema definition
  - naming conventions
  - glossary

### Skill / Agent Workflow
- ChatGPT Projects, Custom GPTs, and Deep Research are framed as execution surfaces rather than canon.
- GPT acts as parser, mapper, and analyzer over external canon.
- Workflow is repeatable and systematized rather than ad hoc.

## Independent Review
This batch is one of the clearer architectural answers to the question: where should UMG really live? It strongly argues that UMG should live in governed external files and that model runtime should only consume selected projections of that canon. That makes it highly valuable for:
- persistent architecture design
- documentation/governance planning
- future loader/compiler design
- privacy and bounded exposure strategy

Its main limitations:
- object schema is not finalized
- NeoStack definition remains shallow
- loader protocol syntax is still conceptual
- the balance between local-first privacy and hosted convenience is not resolved

This should therefore be treated as strong evidence for system direction, not as final schema or compiler law.

## Roadmap Mapping
- **PHASE_1_CORE_ALIGNMENT:** canon versus runtime separation, object identity, governance principles
- **PHASE_2_COMPILER_IMPACT:** ID-based loading, dependency resolution, missing-object handling, loader design
- **PHASE_3_DOCUMENTATION_IMPACT:** schema docs, naming conventions, glossary, file-structure guidance
- **PHASE_4_SKILL_ALIGNMENT:** GPT as parser/mapper/analyzer over external canon
- **PHASE_5_PRD_AND_STAGING:** local-first registry, canonization workflow, staged deployment surfaces

## Action Outcome
- Accepted as evidence.
- Default four-file pack created.
- Optional extracts created only for:
  - compiler/runtime pressure
  - sleeve extraction
  - neostructure / layered storage-state pressure
  - contradiction / ambiguity tracking

## Recommended Next Decision
Decide whether the project wants to formally lock a one-object-per-file schema and loader contract now, or continue refining object fields and loading semantics before freezing them.

# BATCH-006 — Reviewed Batch
## Batch Overview
- **Batch ID:** BATCH-006
- **Short Topic:** authority resolution, runtime alignment, compiler/display metadata
- **Source Type:** extracted chat summary with project-file references
- **Disposition:** evidence only, not canon
- **Primary Domain:** compiler/runtime alignment
- **Optional Extracts Included:** compiler, sleeve, blocks/MOLT, neostructure

## Source Snapshot
- The batch centers on aligning UMG theory, current compiler behavior, runtime expectations, and project-mode packaging with minimal churn.
- It grounds the discussion in existing project files covering sleeve semantics, format separation, NeoStack catalogs, and bounded-agency runtime work.
- The dominant concern is that UMG has a strong conceptual authority model, but the current compiler mostly assembles prompts and indexes tags rather than resolving authoritative active truth.
- The batch also introduces candidate metadata/display surfaces such as block headers, display keys, created/updated timestamps, lane index, and in-lane rank.

## Chat-Level Summary
This batch is a targeted alignment pass between current compiler reality and intended UMG runtime behavior. It preserves the existing block/stack/sleeve/MOLT model, but isolates the key missing phase—Authority Resolution—as the bridge between normalization and prompt assembly. It also turns several loose concerns into implementation-ready surfaces: tags vs signals vs conditions, resolved active-state emission, display metadata for editor/compiler UX, and stronger governance-aware runtime semantics.

## UMG-Relevant Extraction
### 1. Core semantic signal
- UMG remains a modular cognition framework built from blocks, stacks, sleeves, NeoBlocks, and NeoStacks.
- The batch keeps cognition separate from output format and keeps authority separate from prompt order.
- Project mode is treated as an orchestration surface rather than a replacement for the underlying architecture.
- Existing project-file definitions are used as grounding rather than reinventing the base terms.

### 2. Compiler/runtime alignment signal
- The current compiler is described as performing validation, normalization, grouping, bundle creation, prompt assembly, tag indexing, and runtime emission.
- The missing capability is authoritative conflict handling before text assembly.
- The batch names **Authority Resolution** as the needed phase between normalization and prompt assembly.
- PromptSpec should eventually consume the resolved active set rather than every compiled block that survives basic normalization.

### 3. Tag/signal/condition signal
- Tags are currently treated mainly as indexes.
- The batch distinguishes tags, runtime signals, condition evaluation, and resolved-state truth.
- Trigger behavior is described as partly descriptive in current outputs rather than fully executable branch switching.
- A future runtime contract is implied: Signal Extraction -> Condition Evaluation -> Authority Resolution -> Prompt Assembly.

### 4. UX/editor metadata signal
- The batch proposes separate display and ordering surfaces:
  - creation order
  - MOLT lane order
  - in-lane rank
- Candidate metadata includes createdAt, updatedAt, createdSeq, displayKey, preview, lane index, in-lane rank, and status.
- This is explicitly framed as editor/compiler UX support rather than a semantic rewrite.

## Independent Review
This batch is high-value because it does not try to replace the existing UMG model. Instead, it identifies where current compiler behavior falls short of that model and proposes the narrowest high-leverage bridge: an explicit Authority Resolution phase. That makes it especially useful for Phase 2 compiler work and for reducing confusion created by “active” outputs that are not yet conditionally resolved.

The strongest project value is the combination of:
- low-churn alignment posture
- clean separation between authority and prompt order
- a staged runtime path from tags/signals to resolved active truth
- implementation-oriented display metadata that supports editor and repo usability

The main caution is that several elements here remain candidate implementation blocks, not finalized canon. The batch is therefore strong Stage 1 evidence, but still belongs in the evidence / alignment stream rather than canonical decisions.

## Roadmap Mapping
- **Phase 1 — Core Alignment:** sharpens distinctions between authority precedence, prompt order, cognition, and output format.
- **Phase 2 — Compiler Impact:** strongly supports adding Authority Resolution, resolvedStates, tag/signal/condition paths, and governance enforcement before prompt assembly.
- **Phase 3 — Documentation Impact:** supports clarifying current compiler limits and explaining tags vs signals vs conditions.
- **Phase 4 — Skill Alignment:** supports project-mode repo packaging, upload-friendly block libraries, activation protocols, and operator-facing guidance.
- **Phase 5 — PRD and Staging:** contributes bounded-agency runtime linkage, audit-trace expectations, and next-version compiler pathing.

## Action Outcome
- Accepted as evidence.
- Frozen into a Stage 1 intake pack.
- Routed toward compiler, sleeve, blocks/MOLT, and neostructure follow-up surfaces.
- Not promoted to canon.

## Recommended Next Decision
Lock the contract for:
1. **Authority Resolution**
2. **resolvedStates emission**
3. **tags vs signals vs conditions**
4. **which display metadata belongs to compiler output vs editor-only UX**

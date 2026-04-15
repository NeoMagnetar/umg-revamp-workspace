# BATCH-053 — UMG Agent Architecture Review

## Batch Overview
- **Batch ID:** BATCH-053
- **Working Topic:** UMG agent architecture, block necessity, runtime mutation, and alignment inheritance
- **Review Status:** REVIEWED
- **Disposition:** ACCEPT_AS_EVIDENCE; NOT_CANON
- **Source Type:** secondary structured summary, not raw transcript
- **Confidence Note:** medium confidence on coverage; lower confidence on exact phrasing or sequence because the underlying chat transcript was not provided directly

## Source Snapshot
- The source describes a chat that shifted from Bolt hackathon strategy into UMG architecture design for agent systems.
- The main focus was not one product build, but a reusable internal logic system for many agents, rooms, and use cases.
- The source explicitly distinguishes exploratory architecture from settled specification in several places.
- Strong evidence surfaces include:
  - five-block necessity audit
  - dynamic mutation model
  - MOLT vs Skeleton dual-template framing
  - alignment architecture options: Mainline, Tether, inheritable Alignment Block
  - specialist relay / frontend-backend split
- Limits:
  - no raw transcript
  - no direct code or repository artifact
  - several ideas remained unratified

## Chat-Level Summary
This batch advances UMG from static modular prompting toward agent-usable architecture. It pressure-tests which blocks are essential, distinguishes stable MOLT usage from adaptive Skeleton-style agents, explores runtime mutation and specialist relay workflows, and asks how alignment should persist across spawned or collaborating agents. The strongest operational signal is to keep both classic MOLT and Skeleton-style templates while treating Primary, Instruction, Merge, Philosophy, and Subject as the current strongest candidate execution core.

## UMG-Relevant Extraction

### Core semantic signal
- UMG is treated as a modular cognition system for designing adaptive agents, not only static outputs.
- The chat frames an agent as a **living loadout** rather than a single prompt.
- Two operational templates are preserved:
  - **classic MOLT** for clarity, stability, and rapid prototyping
  - **Skeleton Agent** for adaptive cognition, evolution, and deeper simulation

### Block taxonomy and necessity
- Discussed blocks:
  - Primary
  - Instruction
  - Philosophy
  - Subject
  - Merge
  - Meta
  - Off
  - Format
  - Memory
- Necessity audit reduces the strongest execution core to:
  - Primary
  - Instruction
  - Merge
  - Philosophy
  - Subject
- Treated as optional / extended:
  - Format
  - Memory
  - Meta
- Treated as likely redundant / legacy:
  - Off

### Trigger and runtime behavior
- Trigger logic appears as adaptive conditions rather than a permanently ratified block type.
- Runtime examples include:
  - user correction rewriting active instructions
  - Merge activating when blocks collide
  - Meta-style rerun when confidence or clarity drops
  - memory or preference triggering tone shifts

### Priority and control
- Priority is handled compositionally rather than as a separate fixed block.
- Merge examples imply precedence logic and scoped overrides.
- Token audit favors Instruction first, Primary second, Merge third for compact utility.

### Governance and alignment
- Three alignment/control directions appear:
  - immutable Mainline / Seedline style anchor
  - local Tethers for small shared context
  - inheritable Alignment Block copied into child agents
- Strongest exploratory direction:
  - Mainline as universal alignment anchor
  - Alignment Block as lineage/local inheritance
  - Tether as limited context-sharing layer

### Architecture and workflow
- Frontend/backend split separates cognition from presentation.
- Relay workflows treat UMG as an agent workflow language, not just a prompt template.
- Research-first staging is favored over immediate full product build.

## Independent Review
This batch is highly valuable for **Phase 1 and Phase 2** because it moves the discussion from descriptive modularity into operational architecture. The most useful contribution is not a final doctrine statement, but a **decision surface**:
1. whether the five-block core is canonical or merely execution-optimized,
2. whether Skeleton is an evolution of UMG or a runtime pattern on top of it,
3. how alignment inheritance should be modeled across related agents,
4. how far runtime mutation can go before auditability and token efficiency degrade.

The source is also duplication-sensitive. It overlaps earlier UMG semantics work on MOLT, Merge, alignment, and agent deployment, but adds sharper distinctions around necessity, inheritance, and multi-agent structure. It should therefore be merged as **evidence enrichment**, not treated as a standalone doctrine branch.

## Roadmap Mapping
- **PHASE_1_CORE_ALIGNMENT**
  - block necessity and role boundaries
  - Trigger status
  - Merge semantics
  - Skeleton vs classic MOLT boundary
- **PHASE_2_COMPILER_IMPACT**
  - mutation tracing
  - relay orchestration
  - protocol support for Mainline/Tether-style constructs
- **PHASE_3_DOCUMENTATION_IMPACT**
  - crucial / optional / redundant block audit
  - UMG vs Skeleton comparison
  - alignment mechanism comparisons
- **PHASE_4_SKILL_ALIGNMENT**
  - research-planning bot
  - archetype starter kits
  - multi-agent workflow skills
- **PHASE_5_PRD_AND_STAGING**
  - research-first staging for Citadel-style product scope

## Action Outcome
- Accepted as evidence-rich intake material.
- Exported default Stage 1 files.
- Exported optional extracts for:
  - compiler/runtime implications
  - blocks/MOLT necessity logic
  - neostructure / multi-agent architecture
  - contradiction flags
- Not promoted to canon.
- No canonical name or final reduced-core decision inferred.

## Recommended Next Decision
Decide whether the five-block set (**Primary, Instruction, Merge, Philosophy, Subject**) is:
1. canonical UMG core,
2. execution-optimized subset of a broader UMG block system, or
3. a Skeleton-mode loadout rather than baseline UMG.

A second linked decision should formalize the relationship between **Mainline**, **Tether**, and **Alignment Block** as system-layer constructs versus block-layer constructs.

# BATCH-066 — UMG Market Agent Stacks Review

## Batch Overview
- **Batch ID:** BATCH-066
- **Topic:** UMG-applied trading and market-intelligence stacks
- **Review status:** REVIEWED
- **Disposition:** ACCEPT_AS_EVIDENCE
- **Source condition:** Structured source summary provided in chat; not a raw transcript
- **General assessment:** Strong Stage 1 evidence for deployable UMG agent stacks, immutable-core runtime design, tethered coordination, and rendering-surface separation

## Source Snapshot
This batch summarized a chat focused on using UMG/PoeUMG as the reasoning and control architecture for real-world trading and market-intelligence systems. Core artifacts included a Universal Stock Trader app plan, trader persona stacks, a tethered Trifecta agent model, chart-image analysis GPT concepts, company meeting / earnings intelligence agents, and experiments with multiple output surfaces such as QR, plaintext CantoCore, JSON, and image blocks.

## Chat-Level Summary
The batch moves UMG from general modular cognition into product-shaped, runtime-oriented agent systems. It introduces a recurring deployment pattern:
1. central immutable core
2. philosophy overlay layers
3. instruction MOLTs
4. metamolt or micro-adjustment layers
5. triggers, thresholds, and logging gates
6. optional multi-agent tethering via shared vault memory

The chat also reinforces a recurring separation between:
- logic artifact and display artifact
- agent identity and execution permission
- immutable kernel and runtime overlays
- analysis agents and execution-capable agents

## UMG-Relevant Extraction
### Strong signals
- UMG is used as a live agent architecture rather than only a prompt framework.
- A deployable-agent pattern appears clearly: **immutable core + overlays + instruction MOLTs + runtime gates**.
- Multi-agent tethering is materially developed through the **Trifecta** model with shared vault coordination.
- Trigger logic is explicit and operational: event-driven updates, threshold-based execution, heartbeat loops, news spikes, upload events.
- Rendering separation is unusually strong in this batch: QR, plaintext, JSON, image blocks, and raw specs are treated as interchangeable surfaces for the same underlying logic.

### Reusable architectural patterns
- **Trader kernel pattern:** preserve core alignment/risk rules, adjust only outer layers.
- **Shared-vault tether pattern:** multiple specialized agents share state and conflict logs.
- **Analysis-before-action pattern:** image analysis, meeting intelligence, and macro context are upstream of action.
- **Bounded execution pattern:** execute only under thresholds, approvals, logging, and relevance ranking.

## Independent Review
This is a high-value Stage 1 batch because it demonstrates how UMG semantics can be converted into product architecture. The strongest contribution is not finance content itself, but the generalizable stack model:
- immutable aligned kernel
- contextual overlays
- modular instructions
- reflective/meta tuning
- thresholded triggers
- shared vault coordination
- explainable output and logging

The batch is especially useful for later compiler and PRD work because it connects block language to backend routes, services, execution gating, and multi-agent convergence. It also shows that output surface can change independently of logic, which has direct documentation and UX implications.

### Cautions
- Many trader persona names and artifact names appear exploratory.
- Metamolt is used functionally, but not deeply normalized.
- Product direction is clear, but technical thresholds, scoring rules, and transport surfaces remain provisional.
- QR transport should be treated as unstable evidence, not as a preferred release path.

## Roadmap Mapping
- **Phase 1 — Core Alignment**
  - Clarifies immutable-core vs overlay distinction for deployable agents
  - Extends UMG semantics into tethered multi-agent coordination
- **Phase 2 — Compiler Impact**
  - Strong evidence for trigger handling, shared-vault state, threshold gating, and service merge logic
- **Phase 3 — Documentation Impact**
  - Supports docs on agent stacks, immutable kernels, and output rendering separation
- **Phase 4 — Skill Alignment**
  - Suggests concrete agent skills: chart analyst, meeting-intelligence agent, tethered trader shell
- **Phase 5 — PRD and Staging**
  - Supplies app skeletons, backend route ideas, staging sequence, and MVP deployment logic

## Action Outcome
- Accept as evidence
- Freeze as Stage 1 artifact pack
- Preserve optional extracts for compiler, sleeve, blocks/MOLT, neostructure, contradictions, and canon candidates
- Do not promote trader personas or QR transport behavior into canon

## Recommended Next Decision
Decide whether the **immutable core + overlays + instruction MOLTs + shared-vault tethering** pattern should be elevated from application-layer evidence into a general UMG deployment pattern for agent products.

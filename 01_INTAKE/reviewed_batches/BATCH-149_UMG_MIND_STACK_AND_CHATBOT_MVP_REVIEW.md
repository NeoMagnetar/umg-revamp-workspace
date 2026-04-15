# BATCH-149 — UMG Mind Stack and Chatbot MVP Review

## Batch Overview
Batch ID: BATCH-149  
Source Type: derived summary / modular chatbot MVP, mind-stack architecture, and dev-tooling consolidation  
Working Topic: UMG Mind Stack, chatbot-builder MVP pivot, block-aware dev tools, multi-domain builder scalability, composable agent identity  
Review Status: REVIEWED  
Disposition: ACCEPT_AS_EVIDENCE

## Source Snapshot
The source is a structured consolidation of a chat that explored whether the full UMG Ultimate Builder could be built on Bolt, then deliberately narrowed scope to a Chatbot Builder MVP for hackathon viability.
During that process the conversation:
- designed a modular UMG chatbot architecture
- introduced the concept of a `UMG Mind` built from blocks instead of one monolithic prompt
- expanded developer tooling around sandboxing, validation, trigger inspection, and AI testing
- mapped a complex external system (eBay) into UMG-style planner categories
- compared marketplace feature blocks to a UMG web-builder structure
- generated a live-editable `UMG Mind Stack` JSON template

Because the source is a derived summary rather than a separately ratified canon decision, it should be treated as strong evidence of MVP direction, layered identity/runtime thinking, and block-aware development workflow, but not as automatic canon.

## Chat-Level Summary
This batch is strongest as the point where UMG becomes explicitly about composable cognition rather than just modular UI or category libraries.
Its central contribution is the phrase and structure:
**UMG Mind = composable identity stack**.

That matters because it replaces the ordinary “single system prompt” paradigm with a layered block stack containing identity, alignment, instruction, philosophy, MOLT core, triggers, memory, and ledger.
This is one of the clearest sources in intake for a system-level cognition model that is still implementation-oriented enough to feed a builder product.

The second strongest contribution is the MVP pivot.
Rather than trying to ship Business + Website + Chatbot Builder all at once, the chat explicitly chose the Chatbot Builder as the practical first product.
That is important PRD and staging evidence.

The third strong contribution is dev tooling.
Category 12 / ELI12 expands the design from “builder UI” into block-aware engineering tools such as sandboxes, validators, intent simulators, and trigger viewers.
That matters for making UMG development safe and testable.

## UMG-Relevant Extraction
Blocks are treated as modular units with:
- identity
- behavior
- logic
- metadata

The source explicitly states that blocks support:
- `editable_fields`
- `code_injection`
- `trigger`
- `snap_config`
- `ledger`
- `canto_overlay`

UMG enables:
- stacking
- snapping
- merging

The source characterizes blocks as “synthetic cognition units” rather than static UI elements.

The strongest architecture contribution is the `UMG Mind Stack`.
The stack is presented as a layered structure containing:
- `VaultHeader`
- `AlignmentCore`
- `InstructionLayer`
- `PhilosophyLayer`
- `MOLTCore`
- `TriggerMap`
- `MemoryConfig`
- `LedgerBlock`

This stack acts as:
- agent identity
- runtime cognition model
- composable bot core

MOLT roles referenced in the source include:
- `Primary`
- `Instruction`
- `Philosophy`
- `Subject`

MOLT is used for:
- identity definition
- behavior control
- domain specialization

“Core MOLT” is described as defining:
- domain
- `style_tags`
- role behavior

Trigger logic is more explicit than in many earlier intake sources.
The source references:
- `trigger.next_block`
- `trigger.type` values:
  - `on_load`
  - `on_click`
  - `on_submit`
  - `on_message`

Trigger chains are used for:
- chatbot flow logic
- block sequencing

The source also proposes trigger-visibility tools such as:
- `Trigger Chain Viewer`
- `Snap Flow Preview`

Priority remains weaker than trigger, but it is present through:
- `snap_config.priority`
- block ordering
- suggestion logic

Merge logic appears through:
- `Smart Merge`
- merge preview tooling
- block diff tooling
- functional combination of block behaviors

Bundle logic is implied through:
- starter stacks
- template stacks
- “Generate with AI” stack creation
but no full bundle schema is finalized.

NeoBlock-style composition is concrete.
Blocks are JSON units combining:
- identity (`block_id`, `label`)
- behavior (`editable_fields`)
- logic (`code_injection`, `trigger`)
- metadata (`ledger`, `canto_overlay`)

The source also establishes implicit sleeve/resleeving behavior:
different bots such as Mercury or Sun Tzu imply different sleeve-like identities.
Resleeving is implied through swapping identity-bearing layers such as:
- `VaultHeader`
- Philosophy
- Tone

Governance/control is distributed but meaningful:
- `AlignmentCore` defines ethics and rules
- `InstructionLayer` defines behavioral constraints and restricted actions
- token limits and safety filters define operational boundaries
- instruction injection panel defines override logic
- ledger tracks edits and origin

Output/render separation is clear:
- block JSON acts as logic/data layer
- React UI acts as render layer
- Canvas + Inspector are UI surfaces
- exports vary by domain:
  - PDF for business
  - HTML for web
  - JSON for chatbot

Compiler/runtime logic is also stronger than average here.
Named runtime functions include:
- `interpretCommand`
- `dispatchAIIntent`

Runtime behavior includes:
- block rendering
- trigger execution
- code injection execution
- chatbot next-block traversal

Proposed dev tools include:
- block validator
- prompt-intent simulator
- code sandbox runner

The MVP pivot is explicit:
full multi-builder scope was reduced to a Chatbot Builder to maximize polish and demo clarity.

## Independent Review
This batch has high Stage 1 value because it contributes one of the clearest articulation points between modular builder architecture and modular cognition architecture.
The strongest contribution is not the UI, and not even the category system.
It is the idea that a chatbot can be assembled as a **Mind Stack** rather than as a giant prompt.

That makes this batch especially important for later sleeve, runtime, and compiler work.

The second strongest contribution is the MVP decision.
The chat does not merely mention narrowing scope; it uses that narrowing to preserve UMG expression while making the product buildable.
That is good staging discipline.

The third strong contribution is the developer-tool layer.
Without validator, sandbox, trigger visualizer, and intent-simulation thinking, the system risks becoming too magical and too unsafe.
This batch instead points toward inspectable tooling.

Main cautions:
- merge logic is still more conceptual than formal
- priority logic is present but not systemically developed
- bundle logic remains loose
- “UMG Mind” depth is partially descriptive and only partially enforced
- MOLT, overlay, and ledger terminology are used with varying levels of rigor

## Roadmap Mapping
Primary domain: composable chatbot identity/runtime architecture and MVP reduction strategy

Roadmap phases touched:
PHASE_1_CORE_ALIGNMENT
PHASE_2_COMPILER_IMPACT
PHASE_3_DOCUMENTATION_IMPACT
PHASE_4_SKILL_ALIGNMENT
PHASE_5_PRD_AND_STAGING
PHASE_7_RELEASE_READINESS
PHASE_8_POST_RELEASE_EXPANSION

Key phase implications:
Phase 1: supports sharper treatment of layered identity, MOLT role placement, and composable cognition.
Phase 2: contributes trigger chaining, snap sequencing, AI intent dispatch, and validator/sandbox/compiler-adjacent tooling.
Phase 3: provides documentation-ready language for UMG Mind Stack and modular cognition architecture.
Phase 4: strongly informs agent workflow, prompt schema, builder assistance, and dev-tool skill surfaces.
Phase 5: contributes one of the clearest PRD pivots toward Chatbot Builder as the first viable MVP.
Phase 7: improves release clarity by narrowing scope while preserving strong UMG differentiation.
Phase 8: preserves future expansion into business and web builders without forcing them into the first release.

## Action Outcome
Accepted as evidence.
Frozen as a Stage 1 intake pack.
Optional compiler extract, sleeve extract, blocks/MOLT extract, canon candidates, and contradiction flags are justified because the source contains a strong layered cognition model, MVP decision logic, runtime tooling concepts, and unresolved schema/merge/priority tensions.

## Recommended Next Decision
Control-room review should decide how to normalize and promote:
1. `UMG Mind Stack` as formal layered identity/runtime concept
2. Chatbot Builder as primary MVP decision
3. trigger-chain and snap-preview tooling expectations
4. relation between MOLT roles and sleeve-like identity layering
5. dev-tool system requirements for safe block-based development

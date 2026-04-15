# BATCH-153 — Minimal Block Editor Primitives Review

## Batch Overview
Batch ID: BATCH-153  
Source Type: derived summary / minimal block-editor primitive and flow-logic consolidation  
Working Topic: Primary / Merge / Instruction primitives, snap-based stack flow, merge modes, minimal viable block editor runtime  
Review Status: REVIEWED  
Disposition: ACCEPT_AS_EVIDENCE

## Source Snapshot
The source is a structured consolidation of an early block-editor design chat.
It narrowed scope to three foundational block types:
- Primary
- Merge
- Instruction

It also established:
- a snap-based vertical flow model
- minimal block schema
- merge modes
- stack-validity rules
- a visual block library / stack representation

Because the source is a derived summary rather than a separately ratified canon decision, it should be treated as strong evidence of early V1 primitive design, stack-order logic, and merge/runtime direction, but not as automatic canon.

## Chat-Level Summary
This batch is strongest as a minimal viable execution grammar.
Its central contribution is radical simplification:
reduce the system to three primitives and make their interaction rules explicit before adding more complexity.

The strongest reusable signal is:
Primary → Merge → Instruction

That matters because it provides a crisp early ordering law for a UMG-compatible editor and suggests a minimal compiler/runtime path:
source blocks begin flows,
merge blocks coordinate multiple inputs,
instruction blocks execute after resolution.

The second strongest contribution is merge formalization.
The batch does not treat merge as a vague overlay concept.
It gives concrete modes:
- PRIORITY
- JOIN
- OVERRIDE
- ECHO

This makes the batch especially valuable as a clean V1 reference point for NeoBlock/NeoStack beginnings.

## UMG-Relevant Extraction
The block system is intentionally reduced to three primitives:
- Primary
- Merge
- Instruction

The flow model is a linear vertical stack with optional multi-input merge.
Primary begins a stack.
Merge aggregates multiple inputs.
Instruction executes after merge resolution.

The source frames blocks as modular units of:
- data
- transformation
- execution

The batch does not explicitly use MOLT labels, but an implicit alignment is present:
- Primary → Subject / Source
- Merge → Directive / Combination layer
- Instruction → Instruction layer

Trigger logic is minimal.
No explicit trigger system is defined beyond stack initiation.
Primary acts as an implicit trigger or start node.

Priority is introduced through merge mode behavior.
A key rule is:
- “Topmost non-null input wins”

This functions as a configurable priority resolution mode inside Merge.

Merge is the central coordination node.
Multiple inputs converge into one output.
Merge modes are:
- PRIORITY
- JOIN
- OVERRIDE
- ECHO

Bundle is not explicitly defined, but stacked blocks act like implicit bundles.

NeoBlock-style composition is concrete through a minimal schema:
- `id`
- `type`
- `label`
- `config`
- `inputs`
- `outputs`

The source also states that blocks are JSON-defined plus visual components.
This is strong output/render separation evidence:
logic as data,
UI as renderable editor representation.

NeoStack architecture is explicit in early form:
- stack is vertical
- Primary starts stack
- Merge aggregates
- Instruction must come after Merge

Multiple Primary blocks can feed one Merge.
Instruction must be last in the basic V1 model.

Governance/control is structural rather than policy-driven:
- Instruction cannot precede Merge
- Merge requires inputs
- Primary is required to initiate flow

Compiler/runtime implications are direct:
- execute top to bottom
- resolve merge before passing forward
- compile vertical stack into sequential execution pipeline
- use snap logic to enforce build-time validity

The source also implies staged rollout discipline:
V1 = only three block types, basic snapping, simple merge logic.

## Independent Review
This batch has high Stage 1 value because it captures a foundational reduction.
Many later systems become richer, but this batch preserves the cleanest early primitive model.

The strongest contribution is not breadth.
It is minimal clarity.
The three-block system offers a simple reference architecture for how an editor, runtime, and compiler might begin before taxonomy expansion.

The second strong contribution is the early merge law.
By formalizing merge as a central coordination node with named modes, the batch gives later engine work something concrete to compare against.

This batch is especially valuable as:
- a baseline primitive set
- a V1 scope lock
- an early NeoBlock / NeoStack reference

Main cautions:
- no explicit trigger system beyond Primary start
- no persistence/state model
- no bundle/group abstraction
- no explicit error handling or fallback logic
- Instruction-last rule may become too restrictive later
- merge edge cases are underdefined

## Roadmap Mapping
Primary domain: minimal editor primitives and early stack-execution grammar

Roadmap phases touched:
PHASE_1_CORE_ALIGNMENT
PHASE_2_COMPILER_IMPACT
PHASE_3_DOCUMENTATION_IMPACT
PHASE_5_PRD_AND_STAGING
PHASE_7_RELEASE_READINESS

Key phase implications:
Phase 1: provides a clean early primitive ontology for Primary, Merge, and Instruction.
Phase 2: offers one of the simplest compiler/runtime baselines for vertical execution and merge evaluation.
Phase 3: provides documentation-ready language for V1 block types and stack-validity rules.
Phase 5: supports PRD staging through a tightly scoped minimal editor.
Phase 7: helps distinguish foundational MVP logic from later richer builder systems.

## Action Outcome
Accepted as evidence.
Frozen as a Stage 1 intake pack.
Optional compiler extract, blocks/MOLT extract, canon candidates, and contradiction flags are justified because the source contains primitive block law, stack order, merge semantics, and explicit unresolved limitations.

## Recommended Next Decision
Control-room review should decide how to normalize and promote:
1. Primary → Merge → Instruction as V1 foundational stack order
2. merge modes as standard early UMG operators
3. whether Instruction-last remains canonical or only V1-scoped
4. when Trigger and Bundle become first-class primitives
5. how this minimal editor model relates to later richer MOLT taxonomies

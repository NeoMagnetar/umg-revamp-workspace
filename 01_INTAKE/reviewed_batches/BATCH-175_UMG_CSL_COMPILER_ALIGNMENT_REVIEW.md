# BATCH-175 — UMG CSL / Compiler Alignment Review

## Source Snapshot
Source: `175 Branch · UMG optimization suggestions 2.txt`

The source is a dense Stage 1 evidence batch derived from a long canon-building and implementation-planning chat. It contains positioning language, taxonomy proposals, compiler behavior, documentation architecture, governance rules, repository strategy, and unresolved terminology tensions.

## Faithful Summary
This batch reframes UMG as a **tech-agnostic Cognitive Specification Layer (CSL)** rather than an agent, runtime, orchestration framework, or prompt system. It separates UMG canon from execution and repeatedly defines the compiler output as **RuntimeSpec + Trace**. It locks or strongly proposes MOLT types, authority order, trigger restrictions, merge rules, stack mechanics, sleeve identity, governance/drift rules, and a section-by-section documentation sequence. It also sketches a greenfield compiler pipeline, a fresh repository strategy (`umg-core`), and a bounded relationship between UMG and external reasoning backends such as TRM.

## UMG-Relevant Extraction
### Semantics
- UMG positioned as a tech-agnostic Cognitive Specification Layer.
- UMG specifies cognition; execution is external.
- Runtime-neutral output contract repeatedly framed as `RuntimeSpec + Trace`.
- MOLT types repeatedly stabilized as Trigger, Directive, Instruction, Subject, Primary, Philosophy, Blueprint, Off.
- Merge treated as an operation rather than a MOLT type.
- Authority order repeatedly asserted as Trigger > Directive > Instruction > Subject > Primary > Philosophy > Blueprint > Off.

### Compiler
- Proposed deterministic v0 compiler pipeline:
  `parse -> validate -> choose snap -> select blocks -> remove Off -> resolve stacks -> apply triggers -> enforce authority -> merge -> validate PrimaryShell -> emit RuntimeSpec + Trace`
- Same-type stack resolution via `(molt_type + stack_key)` with highest `stack_rank` winning and deterministic tiebreak by `block_id`.
- Same-type merge only, with explicit `merge_key` and policy-controlled behavior.
- Trace treated as mandatory and as the audit spine of compliance.

### Documentation / Governance
- Strong canonical documentation sequence established and enforced.
- Glossary treated as authority-bearing.
- No silent redefinition, no synonym creep, no UI-driven reinterpretation.
- Experimental material required to remain explicitly non-canon.

### Repo / Implementation
- Fresh repo recommendation: `umg-core`.
- Old repo treated as archival/history rather than continuing canon authority.
- Replit/direct coding workflow preferred over unreliable agent mode.

## Independent Review
This is a high-value evidence batch for **Phase 1 Core Alignment**, **Phase 2 Compiler Impact**, and **Phase 3 Documentation Impact**. It contains unusually strong candidate language for stable positioning and implementation scaffolding. The batch should not be promoted directly to canon because several items remain in proposal form or contain unresolved naming tensions.

## Contradictions / Tensions
- `stack` remains overloaded between strict compiler meaning and broader human-facing layered grouping language.
- `domain/profile/bundle/preset` remains unresolved as the best human-facing term for cross-type conceptual grouping.
- Snap semantics required repeated refinement, indicating prior ambiguity.
- UI/graph representations are rich but not formalized into stable canon.

## Roadmap Mapping
- **Phase 1 — Core Alignment:** high impact
- **Phase 2 — Compiler Impact:** high impact
- **Phase 3 — Documentation Impact:** high impact
- **Phase 4 — Skill Alignment:** medium impact
- **Phase 5 — PRD and Staging:** medium-high impact

## Disposition
**ACCEPT_AS_EVIDENCE**

Reason:
High-value semantics, compiler, and documentation evidence with explicit unresolved tensions preserved.

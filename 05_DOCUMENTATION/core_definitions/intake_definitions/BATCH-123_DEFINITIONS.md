# BATCH-123 — Definitions Extract

## Terminology Scope Note
These definitions are extracted from a derived specification artifact that presents itself as a locked canonical glossary.
They remain Stage 1 evidence until explicitly promoted elsewhere.

## Core System Terms
**Universal Modular Generation (UMG)**  
A Cognitive Specification Layer that describes cognition structurally and deterministically and compiles authored cognitive structures into RuntimeSpec and Trace.

**Cognitive Specification Layer (CSL)**  
A runtime-independent specification layer that states what cognition is, not how it runs, and emits structured specifications rather than free text.

**MOLT — Modular Operating Language of Thought**  
The typed grammar of UMG that defines semantic position, ordering of influence, legal interactions, and compilation constraints.

## Architecture and Composition Terms
**Block**  
The atomic unit of UMG. Contains authored content, has exactly one MOLT type, may have a role, and is inert until compiled.

**MOLT Types (canonical order)**  
Trigger  
Directive  
Instruction  
Subject  
Primary  
Philosophy  
Blueprint

**Trigger**  
Activation and control signals used to enable, disable, or route cognition.

**Directive**  
Strategic steering of behavior and approach.

**Instruction**  
Rules, constraints, and structural requirements.

**Subject**  
Topical anchoring for what cognition is about.

**Primary**  
Core task intent; what is being attempted.

**Philosophy**  
Values, ethics, tone, or worldview influences.

**Blueprint**  
Structural or stylistic shaping of output.

**Molt Stack**  
A vertical column of blocks ordered by MOLT type; a composition unit that visualizes semantic precedence but does not resolve conflicts.

**Vertical Precedence**  
Higher blocks contextualize lower blocks and shape interpretation without silently removing them.

**Horizontal Alignment**  
Blocks of the same type have equal type-level standing, though outcome may still vary by priorityOrder or governance.

**Bundle**  
A grouping mechanism that preserves individual blocks and priority without synthesizing meaning or altering semantics.

**Merge**  
An explicit synthetic operation that combines multiple blocks into a new block and preserves traceability of sources.

## Role and Participation Terms
**Role (Block Role)**  
Participation descriptor independent of MOLT type.

**PrimaryShell**  
Container output role.

**MergeContributor**  
Role indicating participation in synthesis.

**BlueprintGuide**  
Silent formatting influence role.

**Off**  
Inactive-preserved state or role that excludes a block from compilation without deleting it.

## UI vs Compiler Boundary Terms
**Snap**  
A UI-only visual relationship indicating conceptual relatedness; has no compiler semantics.

**Scope**  
The explicit deterministic set of blocks the compiler evaluates; independent of UI layout.

**Synthesis**  
Controlled combination of cognition at micro-synthesis or macro-synthesis levels, always explicit and traced.

## Downstream Structure Terms
**NeoBlock**  
Compiled representation of one resolved Molt Stack, reflecting ordered blocks, merges, bundles, and governance.

**NeoStack**  
Domain-level grouping of NeoBlocks used for capability or domain organization; not a hierarchy.

## Runtime / Compiler Terms
**Governance**  
Explicit conflict-resolution layer that disables, limits, redirects, resolves conflicts, and breaks ties deterministically.

**Sleeve**  
Static cognitive design container containing blocks, Molt Stacks, governance bindings, and domain groupings, with no execution or state.

**Compiler**  
Deterministic transformer that validates structure, applies governance, resolves ordering, builds NeoBlocks and NeoStacks, and emits RuntimeSpec plus Trace.

**RuntimeSpec**  
Compiled cognitive specification describing what is active, suppressed, tasked, constrained, and routed.

**Trace**  
Forensic record of merges, bundles, governance effects, routing decisions, errors, and warnings.

**Determinism**  
Guarantee that identical input yields identical output through stable ordering, explicit rules, and no hidden randomness.

## Definitional Candidates
Type ≠ Role.  
Snap = UX.  
Scope = semantics.  
Governance is the only mechanism that overrides.  
No governance = no suppression.  
No Trace = not UMG.

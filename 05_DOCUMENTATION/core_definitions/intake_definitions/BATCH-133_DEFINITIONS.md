# BATCH-133 — Definitions Extract

## Terminology Scope Note
These definitions are extracted from a derived integration summary with implementation exposure.
They remain Stage 1 evidence until explicitly promoted elsewhere.

## Core Integration Terms
**compileSleeve**  
Compiler entrypoint that accepts a Sleeve plus TriggerState and returns compile result data including runtime, trace, and error state.

**CompileResult**  
Typed output surface containing runtime, trace, and error indicator behavior.

**LangChain Execution Harness**  
Proposed outer integration layer that executes models, tools, and runtime flow around deterministic UMG compilation.

**UMG Compiles → LangChain Runs**  
Architectural framing that keeps UMG as deterministic specification/compilation layer and LangChain as execution surface.

## Runtime Artifact Terms
**RuntimeSpec / runtime**  
Execution-facing compiled structure produced by the compiler.

**Trace**  
Event record of validation, normalization, governance, selection, and completion.

**PromptSpec / RuntimePromptSpec**  
Derived prompt/render artifacts built from runtime structure after compilation.

**Indexes**  
UI/search-friendly runtime lookups such as block titles, stack names, and normalized tag indexes.

## Control and Selection Terms
**TriggerState**  
`activeTriggerIds: string[]` input surface for activation-related logic.

**PriorityGroup**  
Code-level priority tiers: Override, Explicit, Default, Fallback.

**priorityOrder**  
Tie-break field within the same priority group; lower numeric value wins.

**Bundle Intent**  
Code-level bundle mode: ranked or alternates.

**GovernanceBinding**  
Typed scoped attachment of governance to sleeve, stack, stacks, or block targets.

**GovernanceRule**  
Typed governance rule with conditions, target filters, and effects.

## Composition Terms
**RuntimeNeoBlock**  
Compiled NeoBlock runtime structure containing ordered ids, by-MOLT organization, bundle ids, merge ids, selected primary, and active selections.

**RuntimeNeoStack**  
Compiled stack-level grouping containing id, optional domain key, and NeoBlock ids.

## Definitional Candidates
UMG stays the deterministic brain-spec. LangChain becomes the execution harness.  
UMG compiles → LangChain runs.  
runtime = compiled execution-facing structure.  
trace = event record of how that structure was derived.

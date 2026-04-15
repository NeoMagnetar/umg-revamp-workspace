# BATCH-124 — Definitions Extract

## Terminology Scope Note
These definitions are extracted from a derived consolidation summary.
They remain Stage 1 evidence until explicitly promoted elsewhere.

## Core System / Spec Terms
**UMG**  
A formal, technology-agnostic framework for generating cognition as structure rather than behavior.

**CSL**  
A layer that defines intended cognition independently of execution.

**MOLT**  
The formal structural grammar of UMG; atomic structural language rather than the atomic semantic language.

**Block**  
The atomic semantic unit of UMG.

## Governance / Selection Terms
**TriggerState**  
Explicit declared state input that governance may reference during synthesis.

**Priority**  
Assigned conflict-resolution ordering used only within governance-permitted scope; affects application rather than meaning.

**Selection**  
A synthesis outcome among permitted elements within a pass.

**OFF**  
Explicit exclusion mechanism that removes participation from synthesis without deleting identity.

**Governance**  
Authoritative bounded constraint layer that determines admissibility, OFF, required presence, routing, and categorical priority assignment.

## Composition / Resolution Terms
**Bundle**  
Grouping without semantic fusion; preserves identity and meaning of member blocks.

**Bundle Order**  
Structural evaluation order among peers in context; not semantic authority and not exclusion.

**Merge**  
Explicit semantic fusion that creates new composite intent or structure and remains deterministic and traceable.

**Synthesis**  
Higher-order resolution process or compiler stage that consumes bundles, merges, governance, MOLT, and priority.

**Compiler**  
Deterministic transform pipeline that validates structure, applies governance, resolves ordering, and emits RuntimeSpec plus Trace.

## Output / Runtime Terms
**RuntimeSpec**  
Compiled structural contract describing what is active for execution.

**Trace**  
Forensic record showing how synthesis decisions were reached.

**Blueprint**  
Structural or stylistic output guidance rather than semantic content or execution behavior.

**Runtime Host / Execution Adapter**  
Non-normative actor that updates TriggerState, invokes explicit operations, reruns synthesis, and executes behavior externally.

**Recompile Snapshot / Repeated Synthesis**  
Fresh synthesis pass over declared state as inputs or explicit operations change, used to explain hotswap without collapsing spec into execution.

## Structure / Container Terms
**NeoBlock**  
Compiled resolved structural unit derived through synthesis.

**NeoStack**  
Domain-level grouping of blocks or NeoBlocks, not a pipeline or intrinsic hierarchy.

**Sleeve**  
Full cognitive-specification container containing blocks, stacks, governance bindings, and possible reconfiguration rules.

## Definitional Candidates
Blocks = atoms of meaning.  
MOLT = atomic structural language.  
Priority affects application, not definition.  
Structure may shape meaning, but only authority may deny participation.  
UMG defines cognition; applications decide how to execute it.  
Synthesis produces structure, not behavior.  
Governance defines the non-negotiable boundaries of cognition in UMG.  
Bundling establishes structural evaluation order, not semantic authority.

# BATCH-128 — Definitions Extract

## Terminology Scope Note
These definitions are extracted from a derived summary artifact.
They remain Stage 1 evidence until explicitly promoted elsewhere.

## Core System Terms
**Sleeve JSON**  
The canonical authored source of truth for cognitive structure.

**RuntimeSpec**  
Deterministic compiler-resolved structural output for downstream systems.

**Trace**  
Deterministic forensic record of how compiler output was produced.

**RuntimePromptSpec**  
A proposed official prompt-rendered artifact described as what the model would actually see.

## Structural and Operation Terms
**MOLT Stack**  
Canonical per-stack composition organized by MOLT lanes or types.

**Priority**  
A same-MOLT peer-collision resolution mechanism that does not alter MOLT hierarchy and does not override governance.

**Governance**  
The only override mechanism; affects eligibility and ordering without changing block content.

**Merge**  
An explicit subset operation within a stack that uses declared result blocks and does not equal whole-stack compression.

**Bundle**  
A subset grouping operation within a stack that records grouping or selection structure without automatically inventing new compiler blocks.

**NeoBlock Compression**  
A whole-stack action that compresses an entire stack into a NeoBlock artifact; distinct from subset bundle/merge.

**NeoBlock**  
A stack-level artifact created from whole-stack compression and placeable into a higher-level graph.

**NeoStack**  
A higher-level graph entity containing NeoBlocks and other higher-order structures.

## UI and Metadata Terms
**sleeve.ui**  
Editor-only metadata surface for UI information.

**sleeve.ui.ops**  
A UI-only metadata area used to preserve bundle/merge intent and layout state without contaminating compiler semantics.

## Definitional Candidates
Priority does not change MOLT hierarchy.  
Governance is the only override mechanism.  
JSON is a declarative specification, not imperative code.  
It’s a blueprint, not a script.

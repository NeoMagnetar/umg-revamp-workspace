# BATCH-124 — Contradiction Flags

## Purpose
Flag unresolved tensions, scope boundaries, and possible conflicts surfaced by the batch.

## Flags
### 1. Spec–Implementation Gap
The batch explicitly states that Governance and Synthesis semantics in spec may exceed current compiler-v0 or Studio enforcement.
This is not a contradiction inside the source, but it is a project-level tension requiring explicit documentation discipline.

### 2. Normative vs Exploratory Layering
Layered governance (G1/G2/G3) is explored as useful design material but is not adopted as v0 normative law.
Risk: later summaries may flatten design notes into canon.

### 3. Runtime Host Boundary
Runtime host / execution adapter is introduced as important but non-normative.
Risk: future documents may smuggle host behaviors into core UMG semantics.

### 4. Hotswap / Recompile Semantics
Repeated synthesis and hotswap framing is conceptually clean, but the exact operational mechanism remains partly future-facing.
Risk: documentation may overstate available implementation.

### 5. Workflow Drift
The source notes temporary inconsistency around repo scaffolding workflow (all stubs first vs incremental creation).
Low semantic risk, but useful for process clarity.

## Recommended Handling
Preserve these as explicit tensions in later synthesis.
Do not flatten exploratory governance, runtime host behavior, or future-facing compiler behavior into v0 canon without explicit decision review.

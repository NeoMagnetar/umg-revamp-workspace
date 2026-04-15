# BATCH-157 — Evidence Entry

## Batch ID
`BATCH-157`

## Title
HRM vs UMG comparison

## Source Type
Pasted chat-summary evidence batch

## Reviewed Date
2026-04-13

## Summary
This batch positions UMG as an orchestration architecture that can wrap an external specialist latent solver such as HRM. It contributes a concrete integration pattern in which UMG handles routing, verification, budget, confidence gating, fallback, and audit, while HRM handles narrow solver execution for ARC-like or grid-logic tasks.

## UMG Value
### Semantics
- clarifies UMG as orchestration layer / systems wrapper rather than a single model
- introduces a useful comparison between latent internal reasoning and explicit block-level orchestration

### Compiler / Runtime
- suggests routing rules for specialist solvers
- suggests verifier hooks, bounded retries, budget caps, and explainability shims

### Documentation
- adds candidate language for model-agnostic orchestration and explicit audit
- adds comparison framing for latent solver vs explicit wrapper architecture

### Skills
- adds a candidate local-solver adapter pattern
- adds operator-surface guidance: terminal execution surfaces vs unsuitable helper overlays

### PRD / Staging
- adds staged path from environment validation to wrapped execution to ARC-style submission packaging

## Key Extracted Items
- candidate wrapped module name: `hrm.solver`
- candidate wrapper files: `hrm_cli.py`, `hrm.config.json`, `adapter.ts`
- candidate call flow: Directive / Blueprint → Primary / Subject → Verifier
- candidate control surfaces: confidence gates, bounded retries, cost caps, fallback, explainability shim

## Conflicts or Duplicates
- overlaps with BATCH-155 on modular runtime abstraction and stable interface layering
- overlaps with BATCH-154 on bounded-agency / governed execution patterns, but here the emphasis is solver orchestration rather than privilege boundary handoff
- no direct contradiction isolated inside this single source

## Disposition
`ACCEPT_AS_EVIDENCE`

## Export Relevance
- export candidate for semantics glossary review
- export candidate for runtime wrapper design
- export candidate for documentation section on specialist solver integration

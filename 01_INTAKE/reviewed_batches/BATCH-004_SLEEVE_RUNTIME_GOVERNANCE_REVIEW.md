# BATCH-004 — Reviewed Batch
## Batch Overview
- **Batch ID:** BATCH-004
- **Short Topic:** sleeve simplification, runtime contracts, governance locking
- **Source Type:** extracted chat summary / artifact-derived intake text
- **Disposition:** evidence only, not canon
- **Primary Domain:** sleeve runtime governance
- **Optional Extracts Included:** compiler, sleeve, blocks/MOLT, neostructure

## Source Snapshot
- The batch combines two layers:
  1. a live sleeve-authoring exchange centered on a simplified, non-overwhelming persona sleeve
  2. attached UMG artifacts covering sleeve mechanics, MOLT roles, NeoBlock/NeoStack architecture, bundle policy, governance anchoring, runtime loop, and bounded self-improvement
- The source explicitly distinguishes local sleeve-design choices from broader framework rules.
- The runtime material is detailed but marked draft/whitepaper-level rather than finalized release canon.

## Chat-Level Summary
This batch shows UMG operating in two modes at once: practical sleeve authoring and formal system specification. On the practical side, it demonstrates a concrete “simplify the sleeve” workflow that preserves only identity anchors, triggers, and output constraints. On the formal side, it carries substantial runtime/spec material: typed CTX fields, typed outputs, bundle-level policies, governance-anchor assertions, anti-thrash rules, drift thresholds, and bounded self-improvement constraints.

## UMG-Relevant Extraction
### 1. Core semantic signal
- Blocks are treated as atomic meaning units.
- NeoBlocks are compiled active views with one Primary per stack and layered Instructions.
- NeoStacks are explicit activation units representing work/cognition modes.
- Sleeves define who the system is right now, including defaults, governance, and active stacks.

### 2. Strong runtime/spec signal
- MODE and BP_MODE remain explicitly separate.
- Runtime flow is specified as Initialize -> Goal Genesis -> Goal Selection -> Optional Plan/Execute Hook -> Output Emission -> Runtime Self-Improvement.
- CTX typing and governance-anchor assertions indicate contract-oriented runtime design.
- Bundles are used as real policy containers, not decorative groupings.

### 3. Strong governance signal
- Governance is anchored to POE.UMG.CORE.
- Self-improvement is bounded by explicit prohibitions, thresholds, rollback rules, admissible patch types, and hard governance immutability.
- Safety constraints are embedded in runtime policy rather than bolted on after generation.

### 4. Sleeve-authoring signal
- The live sleeve exchange demonstrates a reduction path from richer persona construction to a lighter essentials-only sleeve.
- “No overlay” and “avoid picture this” function as explicit output constraints rather than broad framework rewrites.
- The batch preserves tension between deterministic full-structure emission and minimal user-facing presentation.

## Independent Review
This batch is highly valuable because it links abstract UMG architecture to an author-facing workflow. It does not just define sleeves and runtime machinery; it shows how a sleeve can be simplified without dissolving identity. That is useful for documentation, skills, and future compiler-facing templates.

The strongest project value is not the persona content itself. The stronger value is the combination of:
- deterministic architecture language
- governance-locked runtime behavior
- a practical authoring pattern for simplified sleeves
- explicit output/rendering separation

The main caution is maturity. The runtime material is detailed enough to influence compiler, documentation, and PRD work, but it is still presented as draft/whitepaper-level input. It should therefore be harvested aggressively as evidence, but not promoted automatically.

## Roadmap Mapping
- **Phase 1 — Core Alignment:** confirms stable language for Block, NeoBlock, NeoStack, Sleeve, MOLT roles, Bundle, and blueprint separation.
- **Phase 2 — Compiler Impact:** supports compile-time enforcement around one Primary per stack, layered Instructions, bundle policy, CTX validation, governance-anchor assertions, and self-improvement admissibility.
- **Phase 3 — Documentation Impact:** supports a formal explanation of simplified sleeve authoring versus full runtime activation.
- **Phase 4 — Skill Alignment:** supports a sleeve-authoring workflow and negative-output constraints as first-class guidance.
- **Phase 5 — PRD and Staging:** contributes PRD-grade inputs through typed contracts, loop structure, drift thresholds, and anti-thrash policy.

## Action Outcome
- Accepted as evidence.
- Frozen into a Stage 1 intake pack.
- Routed toward documentation, compiler, and sleeve-authoring follow-up surfaces.
- Not promoted to canon.

## Recommended Next Decision
Lock the relation between:
1. **full deterministic sleeve/mode activation structure**
2. **minimal user-facing sleeve presentation**
3. **which parts must be compiler/runtime truth versus output-layer simplification**

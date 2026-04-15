# BATCH-102_BLOCKS_MOLT_EXTRACT

## Scope
MOLT / block-role / compositional-structure signals extracted from BATCH-102.

## Expanded Role Inventory
This batch provides one of the broadest role inventories in the intake set:
- Primary
- Instruction
- Guardrail
- Directive
- Trigger
- Subject
- Meta
- Blueprint
- Off

This matters because it pushes UMG beyond the simpler four-role or triad framings and treats audit, shutdown, and invariant control as first-class role surfaces.

## Composition Semantics
The source gives unusually clear distinction pressure between:
- **Bundle** = cohesive grouped execution unit
- **Merge** = layering / extension / combination mechanism

That distinction is valuable because many packets use merge loosely. Here, Merge is used to extend or combine logic after evaluation, while Bundle groups ordered MOLT blocks into reusable units.

## NeoBlock Signal
NeoBlocks are described as containing bundles plus merges of MOLT blocks.

Reported examples:
- `NB.ALIGN.LOVE_LOGIC`
- `NB.STRAT.BRANCH_ENGINE`
- `NB.SAFE.RISK_GATE`
- `NB.AUDIT.RECURSIVE_CORE`

This strengthens the view that NeoBlocks are not merely renamed blocks, but higher-order compositional units with internal structure.

## Invariant / Control Signal
The inclusion of Guardrail, Meta, and Off as role surfaces implies:
- invariants are part of block semantics, not only global system policy
- audit/trace is first-class, not incidental
- termination/shutdown control should be represented explicitly

This has strong documentation and compiler implications.

## Structural Tensions
- the role inventory may conflict with leaner role sets in earlier batches
- Blueprint here leans toward sequence/pipeline definition, which may overlap only partially with earlier style/output framings
- Guardrail may be either a role, a block class, or a system property depending on which packet is considered
- Bundle and Merge distinctions are clearer here than elsewhere, but not yet cross-batch standardized

## High-Value Documentation Targets
- preserve expanded role inventory as a major taxonomy candidate
- define Bundle versus Merge explicitly
- document Meta and Off as first-class structural roles
- clarify NeoBlock as composed-of-bundles-and-merges rather than simple single-block wrapper
- distinguish lightweight public-facing explanations from full advanced role taxonomy

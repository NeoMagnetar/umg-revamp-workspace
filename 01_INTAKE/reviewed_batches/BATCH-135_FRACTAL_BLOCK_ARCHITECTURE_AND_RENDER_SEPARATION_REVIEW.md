# BATCH-135 — Fractal Block Architecture and Render Separation Review

## Batch Overview
Batch ID: BATCH-135  
Source Type: derived summary / UMG-native block construction and compiler-facing architecture consolidation, not a raw transcript  
Working Topic: block-native structure, semantics vs presentation, fractal decomposition, agnostic sleeve plus skillpack architecture, compiler-facing manifests and artifact trees  
Review Status: REVIEWED  
Disposition: ACCEPT_AS_EVIDENCE

## Source Snapshot
The source is a structured consolidation of a chat that moved from presentation-style analysis into explicit UMG-native block construction.
It covered single NeoBlocks, sleeves, NeoStacks, schema blocks, process blocks, compiler-facing backend forms, recursive artifact trees, and domain-specific work systems.
The source also captured a practical frontend constraint: exact typography and spacing cannot be guaranteed through plain chat output, forcing a clean distinction between semantic render structure and actual renderer/UI control.
Because the source is a derived summary rather than a raw transcript or direct implementation bundle, it should be treated as strong evidence of architecture direction, block doctrine, and compiler-facing patterns, but not as automatic canon.

## Chat-Level Summary
This batch is one of the strongest sources for UMG-native artifact form rather than only UMG semantics in the abstract.
Its central contribution is the sharpening of three boundaries:
block meaning versus block presentation,
semantic structure versus renderer control,
and content blocks versus process/schema/trace sub-artifacts.
The strongest practical outcome is a fractal doctrine:
a sufficiently serious block can decompose into internal files, schemas, validators, interfaces, traces, and orchestrators without ceasing to be UMG-consistent.
The batch also provides a clean architectural pattern for mounting specialized work systems into a more agnostic bot sleeve as skillpacks.
The result is high-value evidence for how UMG may become implementation-ready without collapsing into generic prompt templates.

## UMG-Relevant Extraction
UMG is treated as a system for making cognition explicit, modular, auditable, and portable rather than as a writing style.
A NeoBlock is treated as a named, scoped cognitive artifact with explicit role and output contract.
A NeoStack is treated as a multi-domain work architecture rather than a list of traits.
A NeoSleeve is treated as a mountable higher-order specialization layer or skill container.
Schema blocks and process blocks are treated as first-class artifact types.
A strong chat-derived principle is stated:
a serious block deserves its own internal architecture.
The conversation repeatedly rejected generic section reuse when it was not native to the block’s actual function.
Internal module names should arise from a block’s real responsibility, not from universal templates copied across all blocks.
The best-performing examples used explicit internal file trees and sub-artifacts such as:
PhysicsConstraints.block/,
EnergyBudget.schema/,
AuditRun/,
and AZ_Dispensary_Auditor.sleeve/.
A key doctrine is stated:
different artifact classes deserve different internal trees; a NeoBlock is not forced to look internally like a NeoStack or NeoSleeve.
The Arizona dispensary auditor example becomes a clear NeoStack instance with domain folders and a work-process pipeline.
The conversation moves from person/character sleeves toward an agnostic bot sleeve that can host specialized skill cartridges.
Resleeving logic is implied through a stable chassis plus mountable specialized sleeves or NeoStacks.
Governance is treated as a boundary layer rather than a content layer, with input-contract rejection clauses and scope locks.
A strong separation is made between semantic render structure and renderer/UI typography.
Semantic structure can control ordering, labels, line breaks, and section cadence, while exact fonts, weights, spacing, and visual fidelity belong to renderer specification.
A compiler-facing backend representation is proposed using:
block registration/manifest,
typed input contracts,
output contracts,
execution orchestrator,
artifact capture,
validators,
and trace logging.
A strong principle is stated:
adapters translate shape; blocks enforce meaning.
The chat also reinforces boundedness through read-only capture, no covert access, no speculative conclusions, no conclusions without evidence, and phase-gated process authority.

## Independent Review
This batch has unusually high Stage 1 value because it pushes UMG from abstract modularity into artifact-native implementation language.
The strongest contribution is not a single rule but a structural intuition:
UMG scales by recursive containment without flattening everything into one template.
That matters because it gives the project a way to represent serious work systems, forensic intake blocks, compliance sleeves, schemas, validators, and traces under one architectural logic.
The semantics-versus-rendering separation is also important because it prevents typography desires from contaminating block meaning.
That is a very practical doctrine for future Studio and documentation work.
The agnostic-sleeve-plus-skillpack pattern is similarly valuable because it yields a reusable deployment architecture.
Main caution: several examples are strong candidates rather than finalized canon, and some compiler/backend forms were illustrative rather than declared canonical syntax.
The batch should therefore be mined for patterns and doctrine, not treated as a locked implementation spec by itself.

## Roadmap Mapping
Primary domain: fractal artifact architecture and semantic-versus-render separation

Roadmap phases touched:
PHASE_1_CORE_ALIGNMENT
PHASE_2_COMPILER_IMPACT
PHASE_3_DOCUMENTATION_IMPACT
PHASE_4_SKILL_ALIGNMENT
PHASE_5_PRD_AND_STAGING
PHASE_7_RELEASE_READINESS
PHASE_8_POST_RELEASE_EXPANSION

Key phase implications:
Phase 1: reinforces explicit role separation, boundary-layer governance, and block-native section discipline.
Phase 2: provides compiler-facing patterns for manifests, validators, adapters, orchestrators, artifact trees, and trace logging.
Phase 3: gives documentation-ready language for rendering separation, recursive block architecture, and file-tree-bearing artifacts.
Phase 4: supports skillpack mounting and agnostic-chassis deployment patterns.
Phase 5: contributes PRD-level direction for resolver/task-frame/compiler-arbitration separation and implementation-facing artifact classes.
Phase 7: strengthens release-readiness thinking by separating semantic contract from renderer fidelity.
Phase 8: provides a strong pattern for future domain sleeves, blocks, schemas, and mounted work systems.

## Action Outcome
Accepted as evidence.
Frozen as a Stage 1 intake pack.
Optional compiler extract, sleeve extract, neostructure extract, canon candidates, and contradiction flags are justified because the batch contains compiler-facing architecture patterns, sleeve/NeoStack design doctrine, reusable canonical language, and explicit unresolved tensions about rendering and generic template contamination.

## Recommended Next Decision
Control-room review should decide how to normalize and promote:
1. semantics-versus-rendering separation
2. recursive internal architecture doctrine
3. agnostic sleeve plus mounted skillpack pattern
4. compiler-facing manifest/validator/orchestrator language
5. block-native sections versus universal template policy

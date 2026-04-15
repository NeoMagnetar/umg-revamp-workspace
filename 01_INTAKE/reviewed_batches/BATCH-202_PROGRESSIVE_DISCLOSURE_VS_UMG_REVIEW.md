# BATCH-202 — Progressive Disclosure vs UMG — Review

## Batch Overview
- **Batch ID:** BATCH-202
- **Source Type:** derived conceptual comparison summary
- **Review Status:** REVIEWED
- **Disposition:** ACCEPT_AS_EVIDENCE
- **Primary Domain:** interface_architecture_boundary
- **Evidence Strength:** medium
- **Why it matters:** this batch establishes a clean category boundary between UMG as internal cognition/governance architecture and progressive disclosure as an optional surface/interface strategy.

## Source Snapshot
- The source compares “progressive disclosure” to UMG.
- It then asks whether progressive disclosure is still needed once UMG is embodied inside a ClawHub/OpenClaw skill or plugin.
- The conversation resolves toward a layered distinction:
  - UMG = internal architecture and governance
  - skill/plugin = deployment container
  - progressive disclosure = optional interface strategy
- The source is conceptual and documentation-oriented rather than implementation-specific.

## Chat-Level Summary
This batch is a strong **architecture-versus-surface boundary artifact**. Its main contribution is preventing category confusion. It argues that UMG should not be flattened into a UI simplification pattern. Instead, UMG remains the internal system for partitioning cognition, authority, activation, and audit, while progressive disclosure remains a possible external surface technique. That distinction becomes practically useful when discussing agent packaging inside OpenClaw/ClawHub.

## UMG-Relevant Extraction
### Core Semantics
- UMG operates at a different layer than progressive disclosure.
- UMG is framed as:
  - modular architecture for structuring cognition
  - system for control, identity, and execution
  - organized through blocks, stacks, sleeves, and governed activation logic
- UMG is said to organize underlying complexity without requiring it to vanish from the model.

### Roles / Taxonomy
- MOLT appears as a procedural context/reporting frame, not as a disputed framework object.
- Mentioned fields:
  - Trigger
  - Directive
  - Instruction
  - Subject
  - Primary
  - Philosophy
  - Blueprint
- No taxonomy mutation occurs in this batch.

### Runtime / Integration
- Once UMG is embodied as a real OpenClaw skill/plugin, that embodiment is treated as the operational threshold for runtime integration.
- Skill/plugin is treated as the capability container.
- Progressive disclosure is no longer part of core function at that point; it becomes optional surface behavior.
- Full internal structure may remain present even when not foregrounded in UI.

### Governance / Control
- UMG is linked to:
  - governed activation logic
  - partitioned cognition
  - audited cognition
  - internal control independent of interface simplification
- A clean separation is asserted between:
  - internal governance/architecture
  - user-facing control shell

### Output / Surface Separation
- This is the strongest theme in the batch.
- Progressive disclosure is defined as a staged-reveal interface pattern.
- UMG is defined as underlying architecture and control grammar.
- Explicit compatibility model:
  - progressive disclosure may be used inside a UMG-based system
  - progressive disclosure is not equivalent to UMG

### Skill / Agent Workflow
- ClawHub/OpenClaw packaging is described as the deployment vehicle for UMG.
- ClawHub is treated as registry/distribution layer.
- Recommended operator-shell pattern appears:
  - main action path visible
  - current sleeve/state visible
  - active tool lane visible
  - diagnostics and advanced overrides one layer deeper

## Independent Review
This batch is valuable because it clarifies a confusion point that would otherwise distort both documentation and product design. It protects UMG from being misdescribed as a UX simplification pattern and instead keeps UMG at the architecture/governance layer. It is especially useful for:
- documentation language
- FAQ/glossary distinctions
- product-surface decisions
- OpenClaw/ClawHub packaging discussions

Its main limitation is that it remains conceptual:
- disclosure policy is not formalized in schema
- runtime mechanics of OpenClaw/ClawHub are not specified in depth
- no final operator-shell rule is chosen

This should therefore be treated as evidence for explanatory boundaries and product-layer separation, not as final UI law.

## Roadmap Mapping
- **PHASE_1_CORE_ALIGNMENT:** architecture/governance versus presentation distinction
- **PHASE_2_COMPILER_IMPACT:** dormant-but-addressable runtime structure versus UI-only visibility
- **PHASE_3_DOCUMENTATION_IMPACT:** glossary/FAQ language, surface-behavior versus ontology distinction
- **PHASE_4_SKILL_ALIGNMENT:** OpenClaw/ClawHub packaging guidance, operator-shell design
- **PHASE_5_PRD_AND_STAGING:** disclosure policy as product-surface choice rather than runtime dependency

## Action Outcome
- Accepted as evidence.
- Default four-file pack created.
- Optional extracts created only for:
  - compiler/runtime pressure
  - blocks/MOLT taxonomy pressure
  - contradiction / ambiguity tracking

## Recommended Next Decision
Decide whether disclosure policy should remain purely UI/product logic, or whether some operator-surface exposure rules should later become configurable UMG-adjacent surface settings.

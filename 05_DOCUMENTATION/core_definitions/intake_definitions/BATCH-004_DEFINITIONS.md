# BATCH-004 — Definitions Extract
## Terminology
### Block
- Atomic unit of meaning.
- Identity-stable across composition.
- Describes cognition rather than execution.

### NeoBlock
- Compiled active view of blocks inside a stack.
- One Primary per stack.
- Instructions may layer.
- Bundle policy affects activation and ordering.

### NeoStack
- Domain-level aggregation of NeoBlocks.
- Represents a cognition/work mode.
- Explicitly activatable and stateful.

### Sleeve
- Defines who the system is right now.
- Holds governance, active stacks, defaults, and constraints.
- Can also be authored in simplified form while preserving identity anchors.

### Bundle
- Grouping mechanism for ordering, alternation, and policy application.
- In this batch, bundles act as execution-policy containers with explicit constraints.

### Merge
- Deterministic combination of compatible blocks while preserving identity.
- In this batch, merge complexity is locally reduced by removing overlay in the simplified sleeve case.

## Role Language
- **TR / Trigger**
- **DIR / Directive**
- **INS / Instruction**
- **SUB / Subject**
- **PRI / Primary**
- **PHI / Philosophy**
- **BP / Blueprint**

## Architecture Language
- MODE selects cognitive posture.
- BP_MODE selects output emission.
- Governance anchor: POE.UMG.CORE
- Plan/Execute hook: optional tooling bridge
- Anti-thrash lock: runtime stabilization control
- Drift monitor: bounded self-improvement safeguard

## Runtime / Compiler Language
- CTX required fields
- governance_anchor_id assertion
- GoalCandidate / GoalGenesisOutput / GoalSelectionOutput / SelfImprovementOutput
- one Primary per stack
- layered Instructions
- bundle-driven activation / ordering
- admissible patch types
- rollback thresholds
- explicit audit trace

## Definitional Candidates
- “A Block is the atomic unit of meaning.”
- “A Sleeve defines who the system is right now.”
- “Format is controlled independently from cognition.”
- “MODE selects how the system thinks; BP_MODE selects how output is emitted.”

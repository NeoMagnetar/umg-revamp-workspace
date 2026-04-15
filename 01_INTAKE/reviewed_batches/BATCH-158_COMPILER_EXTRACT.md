# BATCH-158 — Compiler Extract

## Compiler / Runtime-Relevant Findings

### Runtime Contract Candidates
The source proposes a typed runtime boundary with objects such as:
- Task
- Plan
- PlanNode
- Observation
- ActionCall
- VSSCheck
- Guard
- ToolSpec
- RunnerContext

This is strong evidence for a reusable UMG runtime contract layer.

### Candidate Compilation Path
1. Intake task
2. Synthesize Plan / PlanNode structure
3. Resolve tools by capabilities
4. Run decide → act → verify loop
5. Apply VSS checks
6. Apply guard decisions
7. Emit events and persist artifacts
8. Permit stop/redirect only at node boundaries

### Overlay / Sleeve Translation
The source implies a compiler-adjacent translation step where sleeves and overlays become runtime modifiers instead of freeform prompt text.

### Guard Compilation
Guard logic appears as structured allow / deny / revise behavior, suggesting a policy compilation surface for action gating and budget enforcement.

### Trigger / Memory Hooks
The trigger scaffold suggests a future compiler/runtime need for persistence-backed trigger registration and controlled rewrite semantics.

## Candidate Tasks
- formalize plan-node DAG or loop structure
- compile overlay/sleeve config into runtime modifiers
- build capability-based tool resolution
- standardize VSS check registration
- add node-boundary stop/redirect semantics
- add artifact persistence and event stream contracts
- define persistence-backed trigger execution

## Confidence
Medium-high for architectural direction; medium for exact implementation because the scaffold is starter code, not verified integrated runtime.

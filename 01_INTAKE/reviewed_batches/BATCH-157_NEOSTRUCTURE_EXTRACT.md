# BATCH-157 — NeoStructure Extract

## Stack Relationship
- UMG sits above HRM as the orchestrator.
- HRM sits inside the larger UMG stack as a specialized reasoning engine.
- UMG decides whether to route a task to HRM or to another engine.
- UMG verifier logic operates after execution to audit or re-score outputs.

## Structural Pattern
This batch contributes a wrapper architecture rather than a fused-model architecture.

### Proposed structure
- planner / strategy layer
- wrapped specialist solver layer
- verifier / audit layer
- fallback / retry governance layer

### Proposed wrapped unit
- one callable specialist engine under UMG control
- invoked selectively by task class
- bounded by cost caps, confidence gates, and retry limits
- auditable through external wrapper traces

## Architectural Value
- preserves UMG identity as orchestrator
- preserves specialist solver efficiency
- allows modular evolution without collapsing system architecture into a single engine

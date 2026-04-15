# BATCH-158 — Evidence Entry

## Entry ID
BATCH-158_EVIDENCE

## Source
- Batch ID: BATCH-158
- Topic: Integrating UMG into Runner
- Source Type: pasted chat extraction / implementation summary
- Review Status: reviewed in Stage 1 intake

## Summary
This batch contributes a concrete pattern for mounting UMG into an Agentic Runner as a doctrine/planning/validation/control layer rather than as a replacement for the runner’s queue-worker-tool substrate. It provides a three-layer architecture, typed runtime contracts, middleware concepts, guard and validation logic, tool abstractions, sleeve/overlay configuration, trigger handling, and a starter scaffold packaged as an integration pack.

## UMG Value
### Semantics
- strengthens the view of UMG as modular cognition and control doctrine
- clarifies the relationship among MOLT, CEL, VSS, Guards, and Overlays inside runtime flow

### Compiler / Runtime
- candidate typed contracts for Task / Plan / PlanNode / Observation / ActionCall / VSSCheck / Guard / ToolSpec / RunnerContext
- candidate plan synthesis and action loop surfaces
- candidate node-boundary stop/redirect behavior
- candidate overlay/sleeve translation into runtime modifiers

### Documentation
- candidate three-layer explanation:
  - Agentic Runner
  - UMG Adapter Layer
  - UMG Kernel
- candidate description of runner as execution muscle and UMG as planning/governance spine

### Skills / Tooling
- candidate runner-facing tool adapters and validation loops
- candidate middleware and eventing expectations
- candidate sleeve / overlay config surfaces

### PRD / Staging
- starter integration scaffold as a milestone artifact
- sanity-check script as an early deployment gate
- observability and persisted run artifacts as staging requirements

## Conflicts or Duplicates
- overlaps with prior bounded-agency and wrapper-pattern batches
- should be merged later with runner/runtime architecture evidence rather than repeated independently
- contains user-specific alignment/vault content that should not be silently promoted into general canon

## Disposition
- Status: ACCEPT_AS_EVIDENCE
- Hold For: cross-batch synthesis on runtime integration architecture
- Export Candidate: yes, for architecture and runtime integration planning

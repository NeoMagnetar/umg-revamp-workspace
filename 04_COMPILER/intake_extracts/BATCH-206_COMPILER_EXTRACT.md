# BATCH-206 — Compiler / Runtime Extract

## Scope
This extract captures the strongest runtime assembly and enforcement semantics preserved in the batch.

## Source-Backed Points
- Runtime assembly:
  - select sleeve
  - load stacks
  - resolve blocks
  - apply permissions and budgets
  - spawn agents
- Assembly includes:
  - dependency checking
  - conflict checking
  - shadowing
  - permission application
  - budget assignment
- The result is an immutable Runtime Context Object (RCO).
- Orchestrator state machine includes:
  - idle
  - assembling_context
  - spawning_agents
  - executing
  - waiting_approval
  - finalizing
  - completed
  - failed
- Deterministic replay depends on:
  - registry snapshots
  - tool call logs
  - artifact checksums
- Agents submit tool intents; they do not call tools directly.

## Compiler / Runtime Pressure
This batch strongly pressures the project toward:
- formal block/stack/sleeve assembly rules
- dependency/conflict/shadowing implementation
- immutable runtime context snapshots
- deterministic replay infrastructure
- approval-state transitions and entitlement validation
- diff/version flows for stack and sleeve mutation

## Conservative Intake Reading
Useful for:
- runtime kernel design
- RCO design
- replayability and observability
- entitlement and budget enforcement

Not enough to:
- settle a full standalone compiler specification separate from runtime assembly
- settle every merge algorithm detail across all block types
- settle every human-versus-agent mutation class

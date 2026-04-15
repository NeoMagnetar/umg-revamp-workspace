# BATCH-158 — Definitions Extract

## Candidate Definitions from Source

### Agentic Runner
The host execution environment responsible for queue, worker, and tool operations.

### UMG Adapter Layer
The thin glue layer between a runner and the UMG kernel, holding contracts, hooks, middleware, and translation logic.

### UMG Kernel
The concentrated UMG logic layer inside the integration pattern, including MOLT, CEL, VSS, Guards, and Overlays.

### MOLT
Mapped here to planning and plan synthesis.

### CEL
Mapped here to action orchestration and run-loop execution.

### VSS
Mapped here to validation gates and checkpointing.

### Guards
Bounded-agency decision layer governing whether actions are allowed, denied, or revised.

### Overlays
Runtime modulation/configuration layer that adjusts heuristics, style, or execution bias without replacing core execution semantics.

### Sleeve
A runtime identity/configuration surface that can package overlays, style biases, and behavior preferences.

### Plan
A structured execution plan produced from task intake.

### PlanNode
A typed node inside the plan, using intents such as gather, transform, decide, act, and verify.

### ToolSpec
A capability-oriented description of a tool surface rather than a prompt-only tool reference.

### RunnerContext
The runtime context object available to planning, orchestration, and validation logic.

### UNDERSTAND > REFLECT > REFINE
A candidate checklist / flow phrase used in the scaffold as a planning/refinement sequence.

### MUTATION: ONLY_IF(SUPERIOR)
A candidate mutation constraint used in the scaffold to limit rewrite behavior.

### TRIGGER > REWRITE.IF.GAIN > THRESHOLD
A candidate memory rewrite / trigger discipline phrase from the scaffold.

## Definition Status
These are source-derived candidate definitions only. They are not canonicalized by Stage 1 intake.

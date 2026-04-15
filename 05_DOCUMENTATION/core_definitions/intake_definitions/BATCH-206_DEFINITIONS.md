# BATCH-206 — Definitions Extract

## Terminology
### Block
Smallest atomic cognitive or functional unit.

### Stack
Ordered collection of blocks forming a higher-level functional layer.

### Sleeve
Active runtime configuration that loads stacks and governs permissions, budgets, philosophy, and mutation posture.

### Runtime Context Object (RCO)
Immutable assembled runtime context produced after sleeve/stack/block resolution and permission-budget application.

### Orchestrator
Runtime kernel that validates tool intents, assembles context, routes work, enforces permissions, and manages approvals.

### Control Room
ChatGPT UI layer for planning, retrieval, and approvals.

### Execution Factory
External orchestrator/API server where real tool-using execution occurs.

## Role / Workflow Language
### Orchestrator Agent
Central coordinating agent; does not merely act as another worker.

### Coder Agent
Primary implementation worker for code tasks.

### Repo Agent
Handles repository-facing operations.

### Research Agent
Performs research and retrieval phases.

### Operator Agent
Bridges local automation and operator-sensitive tasks.

## Governance / Safety Language
### Policy Block
Immutable rule-carrying block encoding hard limits such as no destructive shell or no network write.

### Approval Gate
Required pause/checkpoint before high-risk or privileged actions.

### Shadowing
Higher-priority blocks suppress lower-priority behavior without deleting history.

### Drift Detection
Monitoring for block churn, stack instability, permission creep, or sleeve instability.

## Definitional Candidates
- Blocks = smallest atomic cognitive or functional units.
- Stacks = ordered collections of blocks.
- Sleeves = active runtime configurations.
- Agents never touch the outside world directly. Everything flows through validated tools routed by the Orchestrator.
- ChatGPT UI is the control room; the orchestrator is the execution factory.

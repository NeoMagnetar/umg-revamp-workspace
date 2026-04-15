# BATCH-206 — UMG Server Development Guide — Review

## Batch Overview
- **Batch ID:** BATCH-206
- **Source Type:** derived PRD/runtime architecture summary
- **Review Status:** REVIEWED
- **Disposition:** ACCEPT_AS_EVIDENCE
- **Primary Domain:** orchestrated_runtime_architecture
- **Evidence Strength:** high
- **Why it matters:** this batch operationalizes UMG as a runtime system for coder-first multi-agent work, with persistent Blocks/Stacks/Sleeves, explicit control versus execution planes, bounded tool routing, and staged deployment logic.

## Source Snapshot
- The source centers on a practical UMG-based agent system for coding, repo work, local automation, document retrieval, and ChatGPT UI integration.
- It separates:
  - ChatGPT UI as control room
  - remote MCP as safe gateway
  - orchestrator/API server as execution plane
  - local automation plane for controlled computer tasks
- It provides PRD-style material including runtime concepts, storage, agent roles, tooling, safety, deployment, and follow-on implementation artifacts.
- The source is a structured summary of a long planning session rather than an implemented runtime.

## Chat-Level Summary
This batch is a strong **runtime operationalization artifact**. It moves UMG beyond conceptual modularity into a governed execution design. The key move is treating Blocks, Stacks, and Sleeves as persistent, versioned runtime objects and placing an orchestrator between agents and the outside world. The system becomes:
- deterministic
- auditable
- approval-gated
- bounded by permissions, budgets, and policy blocks
- capable of coder-first multi-agent workflows

This is one of the stronger Stage 1 sources for deployment-facing UMG architecture.

## UMG-Relevant Extraction
### Core Semantics
- UMG runtime is built from three core units:
  - Blocks = smallest atomic cognitive or functional units
  - Stacks = ordered collections of Blocks
  - Sleeves = active runtime configurations
- Blocks can carry philosophy, instruction, policy, tool rules, memory, style, validation, budget, and epistemic logic.
- Stacks act as higher-level functional layers.
- Sleeves govern active stacks, permissions, budgets, philosophy, and mutation posture.
- Runtime assembly is explicitly:
  - select sleeve
  - load stacks
  - resolve blocks
  - apply permissions and budgets
  - spawn agents

### Runtime / Compiler
- A Runtime Context Object (RCO) is produced from assembly and is immutable after creation.
- Runtime assembly includes:
  - dependency checking
  - conflict checking
  - shadowing
  - permission application
  - budget assignment
  - agent spawning
- Orchestrator state machine includes:
  - idle
  - assembling_context
  - spawning_agents
  - executing
  - waiting_approval
  - finalizing
  - completed
  - failed
- Deterministic replay is supported through snapshots, logs, and checksums.

### Governance / Control
- Strong trust boundaries are defined:
  - ChatGPT UI
  - remote MCP gateway
  - API orchestrator
  - local automation plane
  - external services
- Agents never use tools directly; they submit tool intents to orchestrator.
- Approval gates exist for:
  - repo writes
  - PR opening
  - risky shell commands
  - sleeve mutation
- Policy blocks can encode hard constraints such as:
  - no destructive shell
  - no network write
  - no credential exfiltration

### Agent / Skill Workflow
- Coder-first multi-agent roles are defined:
  - Orchestrator Agent
  - Coder Agent
  - Repo Agent
  - Research Agent
  - Operator Agent
- Main workflow:
  - task submission
  - preflight
  - optional research
  - coding phase
  - local validation
  - stabilization loop
  - repo phase
  - approval gate
  - finalization
- Big-task handoff and chunked design/build/handoff work is also emphasized.

## Independent Review
This batch is one of the most practically valuable runtime design sources in the intake set. It gives the project a coherent answer to the question: how does UMG become an actual agent system without collapsing governance? Its strongest contributions are:
- persistent runtime object model
- orchestrator-centered tool routing
- bounded agency through approvals, permissions, budgets, and policy blocks
- clear split between control room and execution factory
- phased build path from MVP to richer orchestration

Its limits:
- “compiler” language is partly runtime-assembly language rather than a fully independent compiler spec
- exact merge behavior is still only partly specified
- ChatGPT-side execution remains intentionally limited
- human versus agent mutation authority is constrained but not fully finalized in all classes

This should therefore be treated as high-value evidence for runtime design and PRD staging, not as already-complete implementation doctrine.

## Roadmap Mapping
- **PHASE_1_CORE_ALIGNMENT:** lock runtime object meanings for block, stack, sleeve, and mutation governance
- **PHASE_2_COMPILER_IMPACT:** runtime context assembly, dependency/conflict/shadowing logic, replayability
- **PHASE_3_DOCUMENTATION_IMPACT:** block/stack/sleeve schema docs, trust boundaries, approval flow, risk classes
- **PHASE_4_SKILL_ALIGNMENT:** role-based agent sleeves, entitlement matrices, coder-first multi-agent workflows
- **PHASE_5_PRD_AND_STAGING:** M0–M3 milestone path, bootstrap order, single-node MVP to broader runtime

## Action Outcome
- Accepted as evidence.
- Default four-file pack created.
- Optional extracts created only for:
  - compiler/runtime pressure
  - blocks/MOLT/runtime-object pressure
  - sleeve extraction
  - neostructure/runtime-layer pressure
  - contradiction / ambiguity tracking

## Recommended Next Decision
Decide whether the next canon-facing step should formalize block, stack, and sleeve schemas plus Runtime Context Object rules, or keep them as PRD/runtime design surfaces until merge and mutation law are tighter.

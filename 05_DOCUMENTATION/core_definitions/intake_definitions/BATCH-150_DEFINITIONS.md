# BATCH-150 — Definitions Extract

## Terminology Scope Note
These definitions are extracted from a derived agent-template and abstraction-layer summary.
They remain Stage 1 evidence until explicitly promoted elsewhere.

## Core Template Terms
**Agent Template**  
Reusable structured schema for composing an agent from layered blocks rather than one monolithic prompt.

**Public Abstraction Layer**  
Simplified user-facing builder surface that hides some internal UMG complexity while preserving structured generation underneath.

**molt_core**  
Central classification block containing fields such as `molt_type`, `domain`, and `style_tags`.

**trigger_chain_map**  
Execution-flow block describing how input is processed and sequenced across the agent.

## Layer Terms
**VaultHeader**  
Identity-defining layer containing fields such as identity, signature, and origin myth.

**Alignment Core**  
Ethics and rule layer defining guardrails and acceptable behavior.

**Instruction Layer**  
Behavior-logic layer defining governance style, primary behavior, and restricted actions.

**Philosophy Layer**  
Worldview or interpretive lens layer.

## Definitional Candidates
UMG supports both internal complexity and external simplification layers.  
A reusable agent is a layered JSON block object, not just a styled prompt.  
Public creators should simplify interface without erasing internal structure.

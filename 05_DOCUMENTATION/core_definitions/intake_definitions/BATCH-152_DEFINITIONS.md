# BATCH-152 — Definitions Extract

## Terminology Scope Note
These definitions are extracted from a derived runtime-bridge summary.
They remain Stage 1 evidence until explicitly promoted elsewhere.

## Core Runtime Terms
**Bounded Bridge**  
Controlled interface through which an agent can execute approved actions against a scoped implementation surface without unrestricted system access.

**Planning Environment**  
The agent’s own reasoning or preparation environment where it determines what should be done before acting.

**Implementation Surface**  
Visible user-facing workspace where changes are reflected, here represented by the browser-hosted IDE.

**Proxy Terminal / Proxy API**  
Execution surface that turns approved agent commands into bounded actions within the workspace.

## Control Terms
**Command Whitelist**  
Restricted set of allowed command prefixes or action types for bridge execution.

**Workspace Scope**  
Filesystem or project boundary within which the bridge is allowed to operate.

**Git-Backed Rollback**  
Use of version control as a recovery and review mechanism for agent-applied changes.

## Staging Terms
**Runtime Mode Split**  
Need to support different startup and execution paths for cloud preview versus local or production hosting.

## Definitional Candidates
The implementation surface is not the agent’s native environment; it is a controlled action surface.  
The proxy terminal acts as the agent’s hands; the browser IDE acts as the visible workspace.  
Plan elsewhere, act through bounded primitives, reflect results visibly.

# BATCH-206 — Contradiction / Ambiguity Flags

## Contradiction Watch
HIGH

## Main Flags
### 1. Compiler vs Runtime Language
The batch uses compiler language loosely; many specifics are runtime assembly rather than a fully separate compiler.

### 2. Merge Algorithm Completeness
Priority, dependency, conflict, and shadowing are described, but a full merge algorithm is not finalized.

### 3. Chat Execution Expectations
The user wants agents working “from chat,” but the design repeatedly limits ChatGPT UI to control-room behavior rather than full execution.

### 4. Mutation Authority Boundary
Agent-driven mutation is constrained by proposal/approval/versioning, but exact class-by-class boundaries are not fully closed.

### 5. Cost / Local vs API Tradeoff
Cheap/free scaling goals remain in tension with API cost, hosted model expense, and local inference complexity.

### 6. Remote MCP Write Boundary
Remote MCP is described as read-mostly or queue-only, but the exact allowed write boundary remains operational rather than fully formalized.

## Intake Conclusion
Use this batch for:
- runtime and orchestrator PRD work
- schema and entitlement planning
- bounded agency architecture
- deployment staging

Do not use it alone to settle:
- final standalone compiler law
- final merge algorithm
- final chat-side execution model
- final mutation authority matrix

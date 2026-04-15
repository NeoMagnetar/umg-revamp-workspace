# BATCH-198 — Contradiction / Ambiguity Flags

## Contradiction Watch
MEDIUM

## Main Flags
### 1. Overlay Count Ambiguity
The source does not define whether only one overlay may be active or whether multiple overlays can stack.

### 2. Overlay Precedence
If multiple overlays are possible, precedence and conflict resolution are not defined.

### 3. Persistence Scope
Persistence is described through system memory, but exact boundary across session, project, or other storage scopes is not formalized.

### 4. Metamolt Interaction
The relationship between overlay behavior and metamolt/logic-spine processes is implied but not formalized.

### 5. Rollback Semantics
Rollback is a behavioral principle in the overlay, but explicit rollback of sleeve-state transitions is not described.

## Intake Conclusion
Use this batch for:
- sleeve layering docs
- overlay runtime modeling
- Resleever terminology
- PRD feature shaping

Do not use it alone to settle:
- final multi-overlay law
- final precedence rules
- final persistence boundaries
- final sleeve rollback model

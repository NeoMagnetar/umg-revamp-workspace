# BATCH-128 — Contradiction Flags

## Scope Note
These are tensions or possible conflicts surfaced by the source.
They are not canon decisions.

## Flag 1
**Topic:** Priority UI drift  
**Tension:** Priority was surfaced in ways that implied hierarchy drift, and the user deliberately reduced or grayed out parts of the UI to avoid conceptual confusion.  
**Why it matters:** Documentation and Studio UX need aligned wording so priority remains same-MOLT-only.

## Flag 2
**Topic:** Bundle/merge vs NeoBlock compression conflation  
**Tension:** The source explicitly separates subset bundle/merge operations from whole-stack compression, implying this was previously at risk of conflation.  
**Why it matters:** Compiler docs, Studio UX, and future PRD language should not blur these operations.

## Flag 3
**Topic:** Runtime targeting ambiguity  
**Tension:** Root app, dead-shell client, and `apps/umg-studio` were repeatedly blurred in implementation workflow.  
**Why it matters:** Release and staging documents should define the real product surface explicitly.

## Flag 4
**Topic:** Proposed artifacts vs current outputs  
**Tension:** RuntimePromptSpec, hash rules, and adapter interfaces were discussed as desirable but not yet fully formalized.  
**Why it matters:** Later summaries must distinguish current compiler behavior from target output standards.

## Flag 5
**Topic:** UI-driven implementation details vs canon  
**Tension:** Mobile drawers, button positions, tab naming, and graph UX were explored pragmatically but are not semantic law.  
**Why it matters:** Intake outputs should preserve them as implementation evidence, not core canon.

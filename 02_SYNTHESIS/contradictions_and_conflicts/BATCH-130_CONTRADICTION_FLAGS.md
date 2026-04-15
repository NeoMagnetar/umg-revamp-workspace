# BATCH-130 — Contradiction Flags

## Scope Note
These are not canon decisions.
They are tensions or possible conflicts surfaced by the source.

## Flag 1
**Topic:** MOLT authority wording  
**Tension:** This batch describes MOLT as authority order while other evidence emphasizes governance as the only override mechanism.  
**Why it matters:** Later synthesis must preserve the distinction between semantic ordering, authority framing, and actual override behavior.

## Flag 2
**Topic:** Implicit singleton bundles  
**Tension:** The source leans toward implicit singleton bundles for compiler convenience while also insisting that semantic interaction begins only when bundle or merge is chosen.  
**Why it matters:** The project needs one stable rule for how raw stacked UI states normalize into compiler-ready segments.

## Flag 3
**Topic:** NeoBlock entry path  
**Tension:** NeoBlock is described both as merge result and as compression of a whole stack.  
**Why it matters:** Implementation and documentation need a disciplined model that permits allowed entry paths without collapsing meanings together.

## Flag 4
**Topic:** Primary merge in v0  
**Tension:** Same-source discussion treats Primary merge as dangerous or discouraged rather than fully ruled in or out.  
**Why it matters:** Per-MOLT merge policy tables will need an explicit decision.

## Flag 5
**Topic:** Trigger merge and advanced trigger logic  
**Tension:** Trigger merge is acknowledged as possible but remains advanced and underdefined for v0.  
**Why it matters:** Trigger complexity could destabilize determinism if not tightly bounded.

## Flag 6
**Topic:** UI terminology drift  
**Tension:** Terms like group, collapse, fold, and stack may continue to drift unless the canonical bundle/merge/collapse distinctions are maintained.  
**Why it matters:** Documentation and builder UX can silently reintroduce old confusion if the formal vocabulary is not enforced.

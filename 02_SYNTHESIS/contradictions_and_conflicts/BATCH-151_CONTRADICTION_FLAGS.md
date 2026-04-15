# BATCH-151 — Contradiction Flags

## Scope Note
These are not canon decisions.
They are tensions or possible conflicts surfaced by the source.

## Flag 1
**Topic:** Mergeable Primary vs single Primary  
**Tension:** The source allows mergeable Primaries through `parent_context_mode: "mergeable"` while also preserving strong single-Primary intuitions.  
**Why it matters:** This is one of the most consequential unresolved architecture questions in the system.

## Flag 2
**Topic:** Directive vs Instruction  
**Tension:** Directive is treated as a distinct strategy/mutation layer, but the source also notes overlap with Instruction.  
**Why it matters:** Canon role count and role purity both depend on this decision.

## Flag 3
**Topic:** Philosophy overlap  
**Tension:** Philosophy is defined as ethics/tone, but it can drift toward rule or constraint language.  
**Why it matters:** Philosophy leakage weakens modular separation.

## Flag 4
**Topic:** MCP meaning drift  
**Tension:** MCP is described in multiple ways and remains fluid.  
**Why it matters:** Control-plane vocabulary should stabilize before deep implementation.

## Flag 5
**Topic:** Schema inconsistency  
**Tension:** Fields such as snap config and legacy trigger representations appear in multiple forms across examples.  
**Why it matters:** Schema implementation needs a normalized target before scaling production tooling.

# BATCH-073 — Blocks / MOLT Extract

## Why This Extract Exists
This batch contains a concrete role set and composition surface that are strong enough to justify a dedicated blocks/MOLT extraction.

## Explicit Role Surface in Source
- `Primary`
- `Subject`
- `Merge`
- `Instructions`

## Structural Pattern
Each block was represented as an object with:
- `type`
- `description`

This creates a simple role-plus-payload composition model.

## MOLT Alignment Notes
### Strong Alignment
- Primary present
- Subject present
- Merge present
- Instruction-like role present

### Incomplete or Divergent Areas
- `Instructions` appears as a UI label rather than a singular role label
- Blueprint is not explicitly present
- Priority is absent
- Role relationships are not enforced in the UI

## Bundle / Stack Implications
- Loadout behaves as a grouped block bundle
- Ordered block arrays suggest proto-stack behavior
- Exact canonical mapping remains unresolved:
  - loadout vs bundle
  - loadout vs NeoStack
  - UI block list vs runtime stack

## Stage 1 Conclusion
This batch is useful evidence for a practical MOLT-facing UI layer, but it does not settle final role taxonomy or role law.

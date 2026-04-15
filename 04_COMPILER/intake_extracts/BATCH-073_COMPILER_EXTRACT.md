# BATCH-073 — Compiler Extract

## Why This Extract Exists
This batch is compiler-adjacent because it presents a concrete user composition surface that appears to feed later execution or deployment, even though the actual runtime engine is not implemented in the source.

## Source-Backed Compiler / Runtime Signals
- Implied pipeline:
  - UI
  - loadout assembly
  - save
  - export
  - external execution
- Export packaging suggests downstream consumption of:
  - loadouts
  - blocks
  - token logic
  - JSON state
- Merge exists as a selectable type but not as implemented execution law.
- Priority is absent despite being a known area of concern relative to broader spec expectations.
- No preview, ordering contract, or execution resolver is formalized.

## Candidate Surfaces for Later Synthesis
### Pre-Runtime Assembly Layer
- User composes block arrays in the UI.
- This looks like a frontend assembly surface for later normalization or compilation.

### Persistence Layer
- Saved loadouts act like serialized compositions.

### Export Boundary
- Template generation implies a packaging step where assembled structures leave the UI and move into another system.

## Gaps / Open Implementation Questions
- How should block order affect execution?
- Is loadout serialization equivalent to NeoStack serialization?
- How is Merge resolved at runtime?
- Where does Priority enter the model?
- Should Blueprint be required before export?
- What validates exported configurations before deployment?

## Intake Disposition
Useful compiler evidence, but not a compiler spec.

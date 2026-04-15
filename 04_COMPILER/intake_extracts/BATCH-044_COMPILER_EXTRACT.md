# BATCH-044 — Compiler Extract

## Runtime / Compiler Signal
- distinguish default conversation from explicit `BP_MODE`-bound structured output
- preserve an initialization control surface for sleeve / stack / governance / artifact operations
- treat mode selection and format selection as orthogonal runtime controls

## Candidate Compiler / Runtime Tasks
1. Define a formal state for unbound conversation versus explicit blueprint-bound mode.
2. Preserve base-sleeve detection in initialization status output.
3. Keep mode and format as separate runtime selectors.
4. Support deterministic artifact compilation as an explicit action surface.

## Risks
- `unbound conversational state` is useful but under-specified
- later richer batches may supersede this batch as the deeper source of the same rule

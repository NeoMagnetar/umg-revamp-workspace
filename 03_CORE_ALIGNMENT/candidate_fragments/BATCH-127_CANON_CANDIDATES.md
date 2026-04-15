# BATCH-127 — Canon Candidates

## Status Note
These are candidate canonical fragments extracted from a derived milestone summary.
Inclusion here does not itself promote them to canon.

## Candidate Fragments
1. UMG defines what cognition is.
2. The compiler defines how that cognition is structured.
3. Execution remains external.
4. The compiler is intentionally headless.
5. No UI, no framework bindings, no opinionated runtime.
6. The compiler does not call LLMs, generate text, execute prompts, or perform inference.
7. It only structures cognition.
8. RuntimeSpec and Trace are the key public compiler outputs.
9. `compileSleeve` should remain the canonical public compile entrypoint.
10. The compiler repo should be treated as a canonical implementation linked from the UMG repo.

## Promotion Caution
Before canon lock, compare these fragments against:
actual repo state,
existing spec language,
prior compiler and glossary batches,
and any future wording adopted in release-facing docs.

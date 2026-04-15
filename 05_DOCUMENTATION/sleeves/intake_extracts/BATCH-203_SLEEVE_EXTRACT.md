# BATCH-203 — Sleeve Extract

## Scope
This extract captures sleeve identity and loading behavior in the external-canon model.

## Sleeve Reading
- Sleeves are structured objects linking blocks.
- Sleeves operate as execution context or lens.
- Resleeving is implied through selective loading of different sleeves per session/runtime.

## Storage Model
- Sleeves are discrete objects stored outside the model.
- Sleeves are loaded selectively into runtime.
- Runtime should not assume undeclared sleeve contents.

## Governance Principle
- Chat/runtime sees fragments, not the whole system.
- Sleeve loading should be explicit and bounded.
- Missing referenced components should be marked, not fabricated.

## Project Relevance
Useful for:
- sleeve storage docs
- runtime lens/loading docs
- bounded projection strategy
- resleeving through selective activation

# BATCH-207 — Sleeve Extract

## Scope
This extract captures sleeve identity and sleeve-facing runtime inspection.

## Sleeve State
- `vault/sleeves/PoeSleeve.json` is treated as the active sleeve identity file.
- `/sleeve` route is intended to return the current runtime sleeve.

## Sleeve Reading
Sleeve may contain:
- directives
- persona
- modules
- mode
- tone / philosophy-like fields

## Resleeving Pressure
- future sleeve switching or dynamic sleeve loading is implied
- browser UI may later display or switch sleeve information
- runtime architecture assumes sleeve data is vault-loaded and available to the agent

## Control / Boundaries
- sleeve state is inspectable
- alignment-protected mutation boundaries are preserved
- sleeve behavior is part of the shared runtime brain, not an isolated UI artifact

## Project Relevance
Useful for:
- sleeve runtime docs
- Poe UI inspection features
- future dynamic sleeve switching design

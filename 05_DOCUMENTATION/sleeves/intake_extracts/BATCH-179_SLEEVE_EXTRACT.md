# BATCH-179 — Sleeve Extract

## Scope
Sleeve identity and sleeve-aware repo restructuring signals extracted from the source.

## Direct Sleeve Signal
The source explicitly centers on a three-sleeve Poe architecture:
- `poeCliAgent.ts`
- `poeWebAgent.ts`
- `poeAssistantAgent.ts`

## Structural Meaning
Sleeve separation is treated as a real repo refactor target, not just a naming convention.
The rename from `poeRuntimeAgent.ts` to `poeCliAgent.ts` is a concrete sleeve identity clarification.

## Resleeving / Migration Signal
The broader refactor plan assumes old mixed runtime logic should be redistributed into better-separated sleeve files and supporting routes/scripts.

## Useful Value
This batch is especially valuable because it grounds sleeve separation in implementation structure: files, scripts, routes, seats, and migration stages.

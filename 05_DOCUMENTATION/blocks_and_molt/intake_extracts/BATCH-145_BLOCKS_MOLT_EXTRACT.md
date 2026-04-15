# BATCH-145 — Blocks and MOLT Extract

## Scope
Block- and MOLT-structure signals extracted from the builder-policy source.

## Direct MOLT Signal
The source explicitly uses `molt_type` in block metadata.
Surfaced values include:
- `Primary`
- `Instruction`
- `Philosophy`
- `Subject`

## Visibility Problem
The user stated that current blocks did not visibly express MOLT enough.
This makes MOLT visibility itself part of the batch’s evidence value.

## Proposed UX Response
The assistant proposed a “MOLT Lexicon HUD” / “View MOLT” mechanism so users could:
- inspect normal block meaning
- inspect UMG/MOLT meaning
- understand how specific fields relate to block structure

## Structural Doctrine Signal
- keep blocks usable for casual front-end users
- keep blocks meaningful for developers and back-end users
- preserve rich internal structure without forcing it into the default surface
- expose MOLT deliberately rather than leaving it implicit

## Useful Example Signal
This batch is especially useful not because it expands the number of MOLT roles, but because it highlights the problem of MOLT invisibility inside practical builder systems and proposes a concrete inspection surface as a remedy.

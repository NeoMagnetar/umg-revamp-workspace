# BATCH-194 - Compiler Extract

## Scope
Compiler- and runtime-facing implications extracted from the Bolt integration source.

## High-Value Compiler Claims
1. Candidate runtime engine functions preserved in the source include:
   - `load(id)`
   - `canSnap(target, incoming)`
   - `mergeBlocks(a,b)`

2. The source expects block JSONs under real runtime lookup paths such as:
   - `/data/<id>.block.json`
   - `/data/blocks/<MOLT>/<id>.block.json`

3. The source suggests loader behavior reading:
   - `public/data/blocks/**/*.json`

4. Runtime alignment depends on:
   - real file names
   - real block IDs
   - real block JSON presence
   - one active app root

5. Explicit runtime failure preserved in the source:
   - Unexpected end of JSON input during drag/drop parsing

## Likely Compiler Audit Targets
- canonical builder block loader contract
- naming/path conventions for block JSON
- manifest application against real assets
- drag/drop serialization and parse safety
- hot-reload behavior for block assets
- route and app-root correctness

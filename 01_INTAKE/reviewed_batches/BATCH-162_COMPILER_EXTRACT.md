# BATCH-162 — Compiler / Runtime Extract

## Runtime Bug Signal
The original overloaded runtime file behaved as a CLI program:
- executed `main()`
- invoked terminal prompt flow

The web route instead expected:
- imported module behavior
- exported `handle()` contract

## Compiler / Runtime Implications
- sleeve entrypoints should have explicit runtime contracts
- CLI sleeves must not auto-run when imported by web/server surfaces
- shared decision logic should be factored into import-safe modules
- `uiServer.ts` should target the web sleeve explicitly
- assistant/background surfaces should be added as separate entrypoints, not branches inside one monolith

## Candidate Tasks
- extract `decideAction()` into shared core
- separate CLI, web, assistant entrypoints
- enforce import-safe runtime boundaries
- document entrypoint contracts for each sleeve surface
- test CLI and web flows independently after refactor

## Stage 1 Judgment
High value for runtime modularity and packaging discipline; not yet canonical because exact module boundaries remain proposed.

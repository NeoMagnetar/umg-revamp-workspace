# BATCH-207 — Compiler / Runtime Extract

## Scope
This extract captures the strongest runtime assembly and route-consistency implications from the vault snapshot.

## Source-Backed Points
- `loadVault.ts` becomes the canonical runtime loader.
- `vaultLoaderMiddleware.ts` is refactored to wrap `loadVault()`.
- `/memory`, `/stack`, and `/sleeve` move toward `req.vault` access for consistency.
- `injectContext.ts` builds prompt/runtime context from:
  - alignment
  - overlay
  - instruction
  - philosophy
  - mythos
  - repo summary
- `repoScanner.ts` and `scanCLI.ts` build repo-awareness context.
- `describeCLI.ts` inspects files through repo index.
- `commandRouter.ts` handles natural-language runtime routing.
- Browser UI plans reuse `poeRuntimeAgent.ts` and `commandRouter.ts`.

## Compiler / Runtime Pressure
This batch strongly pressures the project toward:
- one canonical cognition loader
- shared route/runtime state via middleware
- reusable runtime brain across CLI and web surfaces
- explicit command-routing semantics
- repo-awareness as first-class runtime context

## Conservative Intake Reading
Useful for:
- route consistency
- runtime context assembly
- Poe browser-shell planning
- repo-awareness integration

Not enough to:
- settle final CLI redesign
- settle all runtime contracts
- validate every generated patch or bundle

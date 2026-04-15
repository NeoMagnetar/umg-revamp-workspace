# BATCH-162 — NeoStructure Extract

## Proposed Runtime Structure
A shared-core plus multiple-sleeve architecture.

## Candidate Layout
- `scripts/lib/poeCore.ts`
- `scripts/lib/gptReply.ts`
- `scripts/lib/commandTools.ts`
- `scripts/lib/injectContext.ts`
- `poeCliAgent.ts`
- `poeWebAgent.ts`
- `poeAssistantAgent.ts`
- `uiServer.ts`
- `public/`

## Structural Principles
- shared cognition belongs in reusable library modules
- UI assets remain separate from backend route handling
- server adapter should import the web sleeve, not the CLI sleeve
- sleeves should be thin shells around the shared core
- runtime entrypoints should be explicit and non-overlapping

## Architectural Value
This is a practical embodiment of modular cognition:
- one core
- many sleeves
- surface-specific runtime contracts
- reduced accidental cross-context execution

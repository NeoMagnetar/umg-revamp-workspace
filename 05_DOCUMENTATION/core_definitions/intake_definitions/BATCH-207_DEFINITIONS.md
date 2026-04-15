# BATCH-207 — Definitions Extract

## Terminology
### Vault
Modular cognitive storage layer for Poe/UMG runtime.

### Canonical Vault Loader
`loadVault.ts` as the single source of truth for loading cognitive state.

### RepoIndex.v1.json
Repo-awareness context artifact extending Poe’s cognitive state.

### ActiveStack.json
Runtime stack file representing current active stack composition.

### PoeSleeve.json
Sleeve identity file representing the current active Poe sleeve.

## Runtime Layer Language
### InstructionLayer
Active instruction stratum used in runtime prompt/context assembly.

### OverlayModules
Overlay/runtime modifier stratum used in prompt or cognition injection.

### MythosBlock
Mythos/context identity block inside vault cognition.

### AlignmentBlock
Protected alignment block used as a bounded-agency control layer.

### MetaMOLT
Runtime metadata surface exposing cantocore-style primary inspection.

## Surface / Routing Language
### commandRouter.ts
Natural-language trigger router for Poe commands, especially ✦-prefixed commands.

### injectContext.ts
Runtime context builder that injects alignment, overlay, instruction, philosophy, mythos, and repo summary.

### Browser-Based Poe Interface
Web UI surface intended to replace brittle terminal interaction while preserving the same backend runtime brain.

## Definitional Candidates
- vault/ is modular cognitive storage
- Poe’s cognition depends on alignment, instruction, overlay, philosophy, mythos, stack, sleeve, and repo awareness
- preserve runtime cognition while changing only the surface layer

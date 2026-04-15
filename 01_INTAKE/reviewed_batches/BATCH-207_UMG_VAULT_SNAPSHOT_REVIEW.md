# BATCH-207 — UMG Vault Snapshot — Review

## Batch Overview
- **Batch ID:** BATCH-207
- **Source Type:** derived runtime/migration summary
- **Review Status:** REVIEWED
- **Disposition:** ACCEPT_AS_EVIDENCE
- **Primary Domain:** vault_backed_runtime_architecture
- **Evidence Strength:** medium-high
- **Why it matters:** this batch operationalizes Poe as a vault-backed UMG runtime by unifying cognitive loading, exposing stack/sleeve/memory inspection, adding repo-awareness, and separating backend cognition from frontend/browser rendering.

## Source Snapshot
- The source centers on stabilizing and extending a Poe-based UMG runtime inside the `neo-umg-mcp-server` repo.
- Main work described:
  - unify vault loading
  - reduce duplicate loaders and legacy `vault.json` usage
  - clean route and CLI integrations
  - add repo-awareness
  - move from brittle terminal interaction toward browser UI and Render deployment
- The source treats `vault/` as modular cognitive storage and distinguishes runtime/control logic from surface rendering.

## Chat-Level Summary
This batch is a strong **vault-backed runtime and migration artifact**. It shows Poe as an agent whose cognition is assembled from vault-loaded alignment, instruction, overlay, philosophy, mythos, stack, sleeve, and repo-awareness files. The strongest move is consolidating cognition loading through one canonical loader and then reusing that runtime brain across CLI, routes, and future browser UI. It also makes runtime state more inspectable by exposing stack, memory, and sleeve views, while preserving bounded mutation and tarball-only external agent workflows.

## UMG-Relevant Extraction
### Core Semantics
- `vault/` is treated as modular cognitive storage.
- Meaningful units discussed include:
  - AlignmentBlock.v1.json
  - InstructionLayer.v1.json
  - MythosBlock.v1.json
  - OverlayModules.v1.json
  - PhilosophyStack.v1.json
  - MetaMOLT.json
  - TriggerSet.v1.json
  - ActiveStack.json
  - PoeSleeve.json
  - RepoIndex.v1.json
- Poe cognition depends on loaded alignment, instruction, overlay, philosophy, mythos, stack, sleeve, and repo awareness.
- Repo awareness is treated as part of cognitive context, not as unrelated tooling.

### Roles / Taxonomy
- MetaMOLT.json is used in stack inspection logic to read cantocore.PRIMARY.
- Runtime categories implicitly include:
  - Alignment
  - Overlay
  - Instruction
  - Philosophy
  - Mythos
  - RepoIndex
- PoeSleeve is treated as the active sleeve identity object.
- InstructionLayer and OverlayModules act as inspectable/switchable runtime strata.

### Runtime / Compiler
- `loadVault.ts` becomes the canonical runtime loader.
- `vaultLoaderMiddleware.ts` is refactored to wrap `loadVault()`.
- `/memory`, `/stack`, and `/sleeve` move toward shared `req.vault` usage.
- `injectContext.ts` acts as runtime prompt builder from cognitive layers.
- `repoScanner.ts` and `scanCLI.ts` generate repo index context.
- `describeCLI.ts` inspects files through repo awareness.
- `commandRouter.ts` becomes natural-language routing logic for Poe.
- Browser UI plans reuse the same runtime brain rather than inventing a second one.

### Sleeve / Stack / Inspection
- `vault/stacks/ActiveStack.json` becomes explicit runtime stack file.
- `vault/sleeves/PoeSleeve.json` becomes active sleeve identity file.
- `/stack` and `/sleeve` are treated as runtime inspection routes.
- Future stack visualizer and sleeve display are planned as surface upgrades on top of the same runtime core.

### Governance / Control
- Alignment mutation is protected in stack mutation logic.
- External codegen agents are bounded:
  - no push
  - no arbitrary code alteration
  - generate scoped files only
  - return tarball/zip only
- Commands are intentionally routed through `commandRouter.ts`.
- Shared loader/middleware becomes a control boundary for consistent runtime state.

### Output / Surface Separation
- Backend/runtime cognition:
  - `poeRuntimeAgent.ts`
  - `commandRouter.ts`
  - `loadVault.ts`
- Frontend/rendering layer:
  - `public/index.html`
  - `client.js`
  - `style.css`
- Browser UI is treated as a better surface on top of the same underlying runtime brain.
- Terminal-to-web migration preserves cognition while changing only the interaction layer.

## Independent Review
This batch is especially useful because it combines runtime stabilization, inspectability, and product-surface migration in one place. It gives a concrete picture of how a vault-backed Poe agent can remain modular while becoming more durable and debuggable. The strongest contributions are:
- canonical vault loading
- stack/sleeve/memory inspection surfaces
- repo-awareness as a cognitive extension
- browser migration without replacing the runtime brain
- bounded external bundle-generation workflow

Its main limitations:
- CLI architecture remained unstable and unresolved
- some patch bundles were flawed in practice
- browser UI remained specified but not finalized here
- some runtime contracts, especially `PoeRuntimeAgent.handle(...)`, were assumed rather than fully normalized everywhere

This should therefore be treated as strong evidence for runtime migration and Poe-facing architecture, not as a completed implementation or final UI contract.

## Roadmap Mapping
- **PHASE_1_CORE_ALIGNMENT:** vault objects as cognition units, Poe sleeve/stack identity, protected alignment boundaries
- **PHASE_2_COMPILER_IMPACT:** canonical loader, req.vault runtime consistency, command routing, context injection
- **PHASE_3_DOCUMENTATION_IMPACT:** vault file roles, inspection routes, runtime brain versus UI surface docs
- **PHASE_4_SKILL_ALIGNMENT:** repo scan/describe abilities, tarball-only codegen workflow, browser-based Poe shell
- **PHASE_5_PRD_AND_STAGING:** CLI-to-web migration, Render deployment prep, staged runtime stabilization

## Action Outcome
- Accepted as evidence.
- Default four-file pack created.
- Optional extracts created only for:
  - compiler/runtime pressure
  - blocks/runtime-layer extraction
  - sleeve extraction
  - neostructure/runtime-layer pressure
  - contradiction / ambiguity tracking

## Recommended Next Decision
Decide whether the browser-based Poe interface should now become the primary product surface, with CLI retained only as a limited maintenance/debug path.

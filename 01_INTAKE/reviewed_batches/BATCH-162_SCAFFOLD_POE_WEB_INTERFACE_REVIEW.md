# BATCH-162 — Scaffold Poe Web Interface Review

## Batch Overview
This batch centers on refactoring Poe inside `neo-umg-mcp-server` from an overloaded single runtime file into a sleeve-based architecture with a shared core and interface-specific entrypoints. The most important UMG signal is the explicit separation between one preserved Poe identity and multiple runtime bodies: CLI, web, and a future assistant/dev surface.

## Source Snapshot
- Source type: chat-derived summary
- Primary topic: Poe web interface scaffolding, runtime debugging, and sleeve separation
- Project relevance: high for sleeve semantics, runtime separation, and bounded local agent workflow

## Faithful Summary
The chat began with practical scaffolding and debugging for a Poe web interface, then shifted into architectural cleanup. The key conclusion was that Poe should not be treated as one overloaded runtime file. Instead, one shared Poe core should inhabit multiple sleeves with different runtime surfaces. The proposed split was:
- `poeCliAgent.ts`
- `poeWebAgent.ts`
- `poeAssistantAgent.ts`

Shared logic was to be extracted into reusable modules such as:
- `scripts/lib/poeCore.ts`
- `scripts/lib/gptReply.ts`
- `scripts/lib/commandTools.ts`
- `scripts/lib/injectContext.ts`

The runtime bug that motivated the split was that a CLI-oriented file executed `main()` and called terminal prompting logic in a context where the web route expected an exported `handle()` function. The stabilized direction was to isolate entrypoints, keep UI/browser rendering separate from terminal prompting, preserve local-only operation, avoid any Git push, and return a tarball for manual extraction instead of remote mutation.

## UMG-Relevant Extraction
### Sleeve semantics
This batch provides direct evidence for a UMG-style sleeve model:
- one preserved Poe identity
- multiple runtime sleeves
- shared cognition/core logic
- interface-specific entrypoints
- resleeving without identity collapse

### Output/runtime separation
The chat sharply distinguished:
- shared cognition/core logic
- CLI prompt flow
- web handler flow
- UI assets in `public/`
- server adapter behavior in `uiServer.ts`

### Bounded agency
The user imposed strict constraints:
- local terminal only
- no GitHub push
- no unrelated edits/deletes
- tarball-only handoff
- scoped refactor rather than uncontrolled repo mutation

## Independent Review
This is strong Stage 1 evidence for sleeve identity and runtime separation. It is especially useful because it does not discuss sleeves abstractly; it ties sleeves to concrete files, entrypoints, and control boundaries. The phrase “Same mind. Different mouths.” is memorable and documentation-worthy, but it remains informal. The strongest technical signal is the distinction between a CLI runtime that auto-runs and a web sleeve that must export a handler. That has direct consequences for future UMG runtime packaging.

## Roadmap Mapping
### Phase 1 — Core Alignment
- strengthens sleeve identity semantics
- supports identity-preserving multi-surface operation
- reinforces separation between core cognition and surface-specific expression

### Phase 2 — Compiler / Runtime Impact
- indicates need for import-safe sleeve entrypoints
- supports shared-core + multiple-entrypoint runtime packaging
- suggests explicit runtime contracts per sleeve surface

### Phase 3 — Documentation Impact
- candidate section: shared core vs sleeve-specific bodies
- candidate explanation: UI/browser rendering is not terminal prompting
- candidate phrase set for sleeve teaching language

### Phase 5 / 6 — PRD, staging, execution
- supports staged manual integration workflows
- validates tarball-based bounded local agent refactors

## Disposition
**ACCEPT_AS_EVIDENCE**

Rationale:
- strong evidence for sleeve separation
- strong evidence for output/runtime separation
- strong bounded-local-execution pattern
- not canon because naming and exact module boundaries remain provisional

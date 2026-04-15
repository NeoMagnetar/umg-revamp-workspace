# BATCH-162 — Evidence Entry

## Batch ID
`BATCH-162`

## Title
Scaffold Poe Web Interface

## Source Type
Chat-derived summary / extracted batch text

## Core Signal
Poe should be treated as one preserved identity with multiple sleeves rather than one overloaded runtime file. Shared cognition belongs in reusable core modules, while CLI, web, and assistant surfaces should be separate entrypoints.

## Key Evidence Points
- explicit sleeve split proposed:
  - `poeCliAgent.ts`
  - `poeWebAgent.ts`
  - `poeAssistantAgent.ts`
- shared core proposed through reusable lib modules
- runtime bug traced to CLI-style auto-execution being imported in a web context
- web flow expected exported `handle()` behavior, not terminal prompting
- local-only bounded workflow required:
  - no push
  - tarball handoff
  - scoped file changes only

## UMG Value
- sleeve semantics
- runtime separation
- output-layer separation
- bounded agency for local agent execution
- migration path from monolithic runtime file to modular agent system

## Risks / Ambiguities
- final code state was not fully validated in-chat
- assistant sleeve remained intentionally minimal / optional
- exact shared-core boundaries remain proposed, not stabilized
- repo path confusion from duplicate extraction affected troubleshooting context

## Disposition
`ACCEPT_AS_EVIDENCE`

# BATCH-155_COMPILER_EXTRACT

## Compiler / Runtime Extract

## Evidence Signal
This batch repeatedly treats the runtime boundary as more important than any specific model backend. The practical contract is an OpenAI-compatible endpoint that lets the agent surface remain stable while the cognition provider changes.

## Candidate Runtime Implications
- Standardize a runtime contract around an OpenAI-compatible API boundary
- Support interchangeable local and remote cognition providers
- Keep model selection runtime-configurable rather than hard-coded
- Isolate provider-specific details behind aliases, adapters, or router logic

## Candidate Compiler / Runtime Tasks
- Define a provider abstraction that normalizes local and remote backends
- Define environment-driven configuration for:
  - base URL
  - API key
  - model alias
- Ensure runtime switching does not require app-layer rewrites
- Preserve optional direct-server and routed-server topologies

## Cautions
- The batch does not define parser semantics
- The batch is runtime-architectural, not compiler-spec-complete
- Router usage remains provisional; do not require it canonically from this source alone

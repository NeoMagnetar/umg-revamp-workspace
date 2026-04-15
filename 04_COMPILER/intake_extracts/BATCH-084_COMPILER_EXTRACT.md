# BATCH-084 — Compiler / Runtime Extract

## Scope
This extract captures the strongest compiler/runtime surfaces preserved in the batch.

## Source-Backed Points
- `CompileMOLT()` is introduced as a compiler/validator stage.
- Its stated purposes:
  - validate block structure
  - normalize block order
  - inject fallback blocks if input is empty or malformed
- `mergeBlocks()` filters out priority-0 blocks, sorts active blocks by priority, and concatenates them into a structured payload.
- `mergeBlocksToTask(blocks)`:
  - compiles blocks
  - concatenates them into a payload
  - derives `taskType` from the Primary block
  - returns payload + steps
- `assembleUMGPayload()` merges preamble + merged blocks into final prompt payload.
- `callLLM()` is the unified model adapter surface.
- `routeStrategy.json` maps model roles and fallbacks.
- Runtime flow includes:
  - input parser
  - logic compiler
  - graph runtime
  - cache/vector retrieval
  - route strategy
  - privacy layer
  - alignment validator
  - memory core
  - output formatter
  - HUD
- Parallelization concepts appear for per-channel compilation and alignment/merge threads.

## Priority / Weighting Surface
- Priority values:
  - 0 = ignored/off
  - 1 = primary
  - 2 = secondary
  - 3 = tertiary
- Token weighting logic:
  - 1 -> 1.0
  - 2 -> 0.5
  - 3 -> 0.25
  - other/default -> 0
- Merge ordering sorts active blocks by ascending priority value.

## Backend / Agent Surface
- `/api/agents/orchestrate` is defined as the backend orchestration endpoint.
- `AgentRunner` is introduced as a frontend caller/display component for orchestration output.
- Task profiles and template agents show runtime specialization pressure.

## Conservative Intake Reading
Useful for:
- compiler task extraction
- route strategy documentation
- fallback behavior design
- backend runtime planning
- config spine normalization

Not enough to:
- settle final canonical runtime
- settle security/privacy implementation details
- settle actual production-readiness claims

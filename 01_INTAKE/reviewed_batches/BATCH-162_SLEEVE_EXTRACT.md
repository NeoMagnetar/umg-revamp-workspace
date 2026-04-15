# BATCH-162 — Sleeve Extract

## Sleeve Signal
This batch is direct evidence for a multi-sleeve Poe architecture.

## Explicit Sleeve Candidates
- `poeCliAgent.ts`
- `poeWebAgent.ts`
- `poeAssistantAgent.ts`

## Key Sleeve Principles
- each file represents a sleeve, not Poe himself
- one identity may inhabit multiple runtime bodies
- interface separation does not imply identity fragmentation
- sleeve names should clarify runtime surface without erasing shared identity

## Runtime Surface Distinctions
### CLI Poe
- terminal-focused
- may run `main()`
- may use prompt tooling such as `inquirer`

### Web Poe
- request/response oriented
- should export a handler such as `handle({ message })`
- should not auto-run CLI prompting

### Assistant Poe
- future background/dev surface
- optional at current stage
- useful for extension without overloading CLI or web sleeves

## Stage 1 Review Note
This batch should inform later canon review around:
- sleeve identity
- resleeving behavior
- naming and runtime surface clarity

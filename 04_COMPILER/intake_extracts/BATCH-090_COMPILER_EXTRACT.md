# BATCH-090 — Compiler / Runtime Extract

## Scope
This extract captures the strongest runtime and parser-related material preserved in the batch.

## Source-Backed Points
- Blocks are assembled first, then interpreted by a parser / UMG engine.
- The conceptual flow described is:
  - user input or intent
  - structured blocks
  - parser / UMG engine
  - LLM
  - specialized agents
  - feedback / iteration
- Specialized agents named:
  - Research Agent
  - Planning Agent
  - Persona Agent
- Agents may suggest or reassemble blocks after execution.

## Compiler / Runtime Pressure
This batch pressures the project toward a simple conceptual runtime diagram that can be reused publicly without overcommitting to implementation specifics. The most reusable form is:
- block assembly
- parser / UMG engine
- LLM
- specialized agents
- feedback loop

## Conservative Intake Reading
Useful for:
- conceptual runtime diagrams
- onboarding and deck visuals
- public-facing parser/execution explanations

Not enough to:
- settle compiler law
- settle serialization format
- settle agent orchestration implementation

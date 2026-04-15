# BATCH-155_NEOSTRUCTURE_EXTRACT

## NeoStructure / Stack Extract

## Layered Stack Observed
- **Core I/O:** Docker Desktop + WSL2
- **Cognition:** Ollama and/or vLLM
- **Protocol:** OpenAI-compatible `/v1`, optionally through LiteLLM Router
- **Memory:** Postgres + pgvector
- **Agent Surface / Envoy:** Poe

## Structural Value
This batch is strong evidence for a modular runtime stack where layers remain replaceable and separately staged. It reinforces that the interaction surface, protocol boundary, cognition backend, and memory layer should not be collapsed into one opaque unit.

## Architectural Principles Surfacing Here
- stable base
- switchable brain
- clean escape routes
- local-first control
- reversible staging
- backend interchangeability

## Intake Caution
These stack labels are useful intake mappings, but they are not yet canonical solely because they appear in this batch.

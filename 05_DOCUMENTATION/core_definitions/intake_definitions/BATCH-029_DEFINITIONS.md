# BATCH-029 — Definitions Extract

## Terminology
### Persona Modulation Layer
- A layer that shapes delivery texture or communication style after cognition is complete.
- Not presented as a MOLT role.
- Not presented as a NeoStack.
- Intended to affect expression, not reasoning content.

### Cognition Layer
- The combined reasoning structure formed by MOLT, NeoBlocks, and NeoStacks.
- Owns method, priority, task structure, and reasoning pathway.

### Trigger Extension
- A typed addition to the Trigger library.
- Example in this batch: business Trigger range `TRG.101–TRG.200`.

## Role Language
- MOLT / NeoBlocks / NeoStacks determine cognition, structure, priority, and method.
- Persona determines delivery texture.
- OpenClaw ingest logic should detect block type and route accordingly.

## Architecture Language
- Persona is a separate modulation layer.
- Trigger files belong inside the Trigger category only.
- Library growth should preserve modular category boundaries.

## Runtime / Compiler Language
- Runtime order:
  1. cognition resolution
  2. blueprint / output format selection
  3. persona modulation
  4. final surface emission
- Persona requires operational metadata for deterministic use.
- Trigger ingest requires exact ID preservation and category fidelity.

## Definitional Candidates
- “personas control how output is expressed without changing what is reasoned”
- “treat persona as a separate modulation layer, not as a MOLT role and not as a NeoStack”
- “solve cognition with MOLT + NeoBlocks + NeoStacks, determine output blueprint / format, apply persona modulation profile, emit final surface text”
- “preserve exact Trigger IDs and category structure during extension ingest”

## Unresolved Definition Edges
- precedence between sleeve defaults and persona modulation
- blend/conflict rules between overlapping personas
- full operational schema for persona runtime enforcement

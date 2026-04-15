# BATCH-023 Definitions Extract

## Terminology

### UMG-instrumented output
Intentional structured output produced by a UMG-controlled runtime layer rather than by baseline model defaults.

### UMG-controlled runtime layer
A runtime posture in which cognition structure and output structure are made explicit instead of left implicit.

### Baseline GPT behavior
Plain conversational model behavior without the additional visible UMG runtime envelope.

### Active sleeve
The declared runtime identity/configuration currently governing the interaction.

### Base Interaction
A lightweight startup posture used at conversation start before heavier task-specific routing or sleeve switching occurs.

### BP_MODE
The active output blueprint / surface-format mode controlling how the response is emitted.

### Bounded startup state
An initialization posture where external actions and memory mutation are explicitly off by default.

## Role / Runtime Language
- Trigger: user asks whether behavior is normal and requests a system check
- Sleeve identity: explicit current runtime frame
- Active stacks: visible runtime posture for audit/explanation work
- Output layer: controlled formatting surface distinct from cognition

## Candidate Definitional Lines
- “You are inside a UMG-controlled runtime layer.”
- “Declared cognition -> mapped intent -> controlled output.”
- “UMG-instrumented output” as the visible result of a structured runtime layer.

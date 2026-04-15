# BATCH-027 — COMPILER EXTRACT

## Compiler-Relevant Signal
- Request interpretation is modeled as intent-based routing.
- Runtime behavior depends on activating the correct stack combination for the user’s task.
- Each stack appears to have a dominant functional role rather than sharing one large undifferentiated response surface.
- Compliance constraints are treated as route-affecting limits, not optional side notes.

## Candidate Compiler / Runtime Implications
### Routing layer
- Support request-type classification that can activate one stack or a stack combination.
- Preserve narrow routing for command-reference questions versus broader design/help flows.
- Allow troubleshooting routes to incorporate domain-delta awareness when failures may be environment-specific.

### Stack / block layer
- Preserve a dominant primary block or equivalent dominant function per stack.
- Avoid flattening stack ownership into a single mixed persona response path.
- Keep runtime competence defined by task activation and support pattern, not static domain memory alone.

### Guardrail layer
- Permit hard restrictions to modify or reject unsuitable response paths.
- Treat compliance-aware constraints as first-class runtime inputs when relevant.

## Candidate Compiler Tasks
- implement intent-based routing from request type to stack combination
- preserve dominant functional ownership per stack
- support restriction-aware response shaping
- keep routing granularity explicit between setup, install, authoring, troubleshooting, reference, and compliance cases

## Compiler Cautions
- The source is architectural and draft-state, not validated against a current implementation.
- No finalized compiler schema is defined in this batch.

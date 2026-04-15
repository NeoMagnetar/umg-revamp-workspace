# BATCH-022 — Definitions Extract

## Terminology
- **Base Interaction:** a low-friction startup mode used when a session begins with minimal user input.
- **Conversation Initialization:** a structured session-start event rather than unstructured greeting handling.
- **Active Sleeve:** the currently declared runtime identity/control frame.
- **Runtime Flags:** visible status indicators such as execution state, external-action state, and memory-mutation state.

## Role Language
- **Trigger:** the event that initiates routing; here, the user greeting.
- **Directive:** the immediate handling requirement implied by the greeting.
- **Instruction:** response behavior constraints for startup handling.
- **Subject:** the current interaction focus, here conversation start / routing.
- **Primary:** the dominant purpose of the turn, here initialization and orientation.
- **Philosophy:** the operating stance; startup favors low overhead and alignment.
- **Blueprint:** the output mode used to emit the response.

## Architecture Language
- **Sleeve:** the layer that defines who the system is right now.
- **NeoStack:** an explicitly activated cognitive/work grouping.
- **Initialization Stack Set:** a lightweight set of stacks used at session start rather than a heavy domain-specific configuration.

## Runtime / Compiler Language
- **Execution: ON:** the system is actively responding.
- **External Actions: OFF:** startup does not authorize external effects.
- **Memory Mutation: OFF:** startup does not write or alter memory.
- **BP_MODE: NL:** the startup output is rendered in natural language.

## Definitional Candidates
- “A greeting can be treated as a structured intake event rather than an exception to the architecture.”
- “Startup posture should be explicit, bounded, and sleeve-visible.”
- “Default initialization prioritizes routing readiness over autonomous action.”

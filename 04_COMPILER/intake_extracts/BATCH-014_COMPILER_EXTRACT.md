# BATCH-014 — Compiler Extract

## Compiler-Relevant Signals
- Request interpretation is already procedural:
  1. parse short MOLT skeleton
  2. determine relevant stacks
  3. apply governance
  4. select blueprint
  5. emit output
- RuntimeSpec adds typed contracts suitable for validation/orchestration.
- Bundle policies are concrete enough to inform deterministic runtime gates.
- Trace outputs are explicit enough to become audit artifacts.
- Inventory pressure in the chat implies need for provenance-aware registry compilation.

## High-Value Compiler Tasks
- validate `CTX` required and optional fields
- compile bundle policy into runtime gates and lock behavior
- generate audit trace outputs named in RuntimeSpec
- separate file-backed registry entries from chat-provisional registry entries
- support inventory views that expose provenance class

## Compiler Risks
- treating chat-generated sleeve registries as canon without source proof
- collapsing sleeve modes into canonical sleeve IDs without explicit mapping
- importing draft runtime material as if final

## Recommended Compiler Stance
- fail closed on provenance ambiguity
- annotate registry origin
- allow draft/runtime artifacts as evidence inputs, not automatic canon

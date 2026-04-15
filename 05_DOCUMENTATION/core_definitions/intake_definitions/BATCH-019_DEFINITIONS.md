# BATCH-019 — Definitions Extract

## Terminology Present In Batch

### Envelope Formatter Skill
A standalone skill surface whose job is to enforce and emit the UMG response envelope rather than explain or reason through the full UMG framework.

### Five-Part Envelope
The visible response contract described in the batch:
- Active Stack
- Envoy Intuition
- MOLT Map
- main prose body
- Metadata / Tags / Help

### Formatting-Layer Skill
A skill scoped to output rendering and section contract enforcement rather than deep semantic understanding or runtime control.

### UMG Understanding Skill
A separate companion skill surface responsible for comprehension, explanation, or framework-level reasoning rather than envelope rendering.

### Main Response Body
The prose-only section of the envelope. The batch explicitly treats this as the only location for ordinary prose content.

### Strict / Compact / Recovery / Paired-Skill Modes
Formatter behavior variants implying:
- strict section fidelity
- compact emission
- recovery behavior after structure failure
- pairing with other skills that supply deeper UMG understanding

## Role Language
- formatter
- explainer
- paired skill
- downloadable package
- installable bundle
- publish artifact

## Architecture Language
- output contract
- presentation layer
- narrow scope
- modular release surface
- composable skill layer

## Runtime / Compiler Language
The batch is light on compiler/runtime semantics. Its main relevant distinction is:
- formatting/output should be separable from deeper cognition / control logic

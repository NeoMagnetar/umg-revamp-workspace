# BATCH-160 — Compiler Extract

## Compiler / runtime-relevant findings
- Scattered UMG notes and repos should be normalized into locked JSON / JSONL schemas before training.
- Dataset conversion scripts are treated as part of the operational pipeline.
- Tool JSON should be validated before execution.
- Runtime should inject Alignment Spine + current Sleeve + Overlay before task execution.
- Telemetry should capture low-quality outcomes and failures for retraining.
- Promotion should be gated by evaluation and alignment preservation.

## Candidate runtime / pipeline implications
### Data normalization
- Convert scattered notes/repos into normalized JSONL with locked schemas
- Build contrastive/corrective pairs from failure cases

### Runtime control
- Enforce schema-valid tool calls
- Use alignment-first system-layer injection
- Preserve failure capture and route into retraining

### Deployment surfaces
- Local GPU short-run path
- Evaluation harness
- Promotion logic
- vLLM/OpenAI-compatible serving
- Space control plane endpoints such as:
  - `/train`
  - `/evaluate`
  - `/promote`
  - `/serve`

## Audit note
This source is strong for pipeline design and runtime surfaces, but several components are starter-grade and require later hardening before they should be treated as implementation-ready.

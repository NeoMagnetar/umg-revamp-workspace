# BATCH-160 — OSS UMG Auto-Training Guide — Review

## Source Snapshot
A pasted source batch covering repo review, canon extraction, training-data planning, fine-tuning workflow, evaluation gates, promotion logic, serving/deployment, and a Hugging Face Space starter pack for an OSS UMG-aligned training pipeline.

## Chat-Level Summary
This batch turns UMG from scattered repo/document material into a staged training and deployment program. It argues that UMG must be unified into a canonical atlas before training, then proposes schemas, datasets, evals, promotion gates, runtime wrappers, and serving surfaces so a model-backed agent can behave in a UMG-disciplined way.

## UMG-Relevant Extraction
- UMG is treated as modular cognition built from self-contained logic units.
- MOLT remains the core substrate, with Snap, Merge, and Stack preserved as central operations.
- Canon unification is treated as a prerequisite for training: atlas/canon, schemas, datasets, evals, runtime wrappers, and deployment surfaces.
- Canonical block roles are preserved, alongside operational support blocks such as Alignment Core, Blueprint, CEL, Chaos Lens, Guardrails, Merge, Meta, Overlay, Tether, UMG.Engine, and VSS.
- Structured JSON schemas are proposed for blocks, sleeves, alignment spines, and training rows.
- A multi-repo architecture is proposed to separate canon, datasets, evals, operator logic, and trainer/deployment surfaces.
- Runtime planning includes Alignment Spine injection, sleeve/overlay injection, schema-validated tool usage, telemetry capture, failure harvesting, retraining, and promotion gating.
- Safety is embedded into dataset design, runtime injection, eval gates, and release promotion.

## Independent Review
This is strong evidence for a future UMG training/deployment stack, not because it finalizes canon, but because it identifies the operational surfaces needed to make UMG reproducible and trainable. The batch is especially valuable where it separates canon from data, data from evals, evals from deployment, and runtime orchestration from model weights.

The strongest unresolved issue is scope control. The source is clear that a canonical atlas is still incomplete, and several scaffold pieces are intentionally starter-grade. That means the batch should be retained as planning and architecture evidence rather than treated as a finished implementation specification.

## Roadmap Mapping
- **Phase 1 — Core Alignment:** strong relevance to canonical atlas creation, block taxonomy, support-block normalization, and schema locking.
- **Phase 2 — Compiler Impact:** strong relevance to normalized JSON schemas, dataset conversion, validation logic, runtime contract enforcement, and tool-call validation.
- **Phase 3 — Documentation Impact:** strong relevance to glossary/index work, repo maps, training/deployment READMEs, and schema documentation.
- **Phase 4 — Skill Alignment:** strong relevance to Poe OS middleware behavior, tool routing, telemetry capture, and sleeve/overlay injection.
- **Phase 5 — PRD and Staging:** especially strong for staged rollout, local GPU development, AutoTrainer/Space deployment, and gate-based release logic.

## Action Outcome
**Disposition:** ACCEPT_AS_EVIDENCE

Default Stage 1 files justified:
- Review
- Evidence Entry
- Project Impact
- Definitions

Optional files justified:
- Blocks/MOLT Extract
- Sleeve Extract
- NeoStructure Extract
- Compiler Extract
- Canon Candidates

Optional files not justified:
- Contradiction Flags
- Canon promotion artifacts

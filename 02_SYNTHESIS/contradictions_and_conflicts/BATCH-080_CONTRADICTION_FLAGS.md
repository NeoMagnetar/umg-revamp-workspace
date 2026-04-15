# BATCH-080_CONTRADICTION_FLAGS

## Contradiction / Ambiguity Flags

### 1. Merge vs RAG Boundary
- Unresolved whether RAG is:
  - a Merge extension,
  - a standalone runtime subsystem,
  - or a hybrid of both.
- This affects compiler design and docs language.

### 2. Static vs Dynamic Merge
- Prior Merge language often assumes additive static content.
- This batch introduces retrieval-backed Merge behavior.
- Canonical Merge semantics may need splitting or subclassing.

### 3. Truth-First Philosophy vs Styling Layers
- The batch sets `TRUTH > STYLE`, but does not define how that interacts with Blueprint or tone shaping under disagreement or uncertainty.

### 4. Runtime Optionality
- Not clear whether retrieval is mandatory when a RAG-enabled block is present or conditional by stack state / query type.

### 5. Retrieval Governance
- Governance is soft here (truth-first, groundedness, transparency), but there is no hard enforcement law for bad retrievals, low-confidence results, or missing evidence.

### 6. Token Budget / Context Pressure
- The batch introduces injection of retrieved material but does not specify overflow handling, truncation rules, or source-priority logic.

## Intake Disposition Note
These flags justify contradiction tracking, but they do **not** justify canon rejection. The batch is still useful evidence for runtime and Merge evolution.

# BATCH-032 — Definitions Extract

## Terminology Present in Source

### Terminal Goal (TG)
The end-state or actual objective the system is trying to accomplish. In this batch, TG is used to stop the system from optimizing a means while losing the real purpose.

### Instrumental Goal (IG)
A subordinate or means-level objective that supports the terminal goal. The source treats confusion between terminal and instrumental goals as a major failure mode.

### ROLES / Semantic Role Binding
A structured way to distinguish acting unit and acted-on unit, such as agent, patient, or instrument. Proposed as a broad semantic anchor rather than a large role taxonomy.

### Activation Constraint (ACT)
A condition or prerequisite that must be satisfied for a plan or answer to be coherent. Used here to model operational preconditions.

### Utility Ordering / U_TARGET
An explicit priority sequence for optimization, such as correctness > safety > time > friction. Proposed to prevent convenience optimization from overriding the actual task objective.

### SUB_PROFILE
A possible structured enrichment layer for Subject, used to represent system purpose, interface mode, or required actor. Raised as optional rather than settled.

### VALIDATE_GOAL_COHERENCE
A proposed deterministic validation pass that checks goal preservation, correct patient/object handling, activation condition satisfaction, and utility ordering before final answer emission.

### Goal–Means Misalignment
The failure mode where the system optimizes a visible means or logistics choice instead of the actual objective.

### Teleological Misbinding
A more formal framing of the same failure family: the system binds to the wrong purpose center.

## Role / Architecture Language

### Broad Types > Narrow Proliferation
Design preference for a few broad semantic anchors instead of many narrow block types.

### Validation Pass > Semantic Bloat
Design preference for correcting coherence through one bounded validator instead of ontology expansion.

### Minimal Extension Framework
A proposal to preserve MOLT’s lightweight nature while adding just enough structure to improve goal coherence.

## Candidate Definitional Notes
- MOLT remains the representation layer, but may need minimal semantic anchors for stronger goal coherence.
- Goal coherence depends on terminal purpose, correct role binding, valid activation conditions, and explicit utility ordering.
- Subject may be too flat for some semantically rich systems, but the source does not finalize whether to enrich Subject or externalize the added structure.

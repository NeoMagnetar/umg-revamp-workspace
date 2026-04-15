# BATCH-035 — Definitions Extract

## Terminology and Role Language

### Trigger Library
- **Observed meaning:** library of activation-oriented atomic blocks.
- **Role language:** answers what activates a reasoning path.

### Directive Library
- **Observed meaning:** library of mission/goal-level control blocks.
- **Role language:** answers what the high-level goal or mission is.

### Instruction Library
- **Observed meaning:** library of specific action-step blocks subordinate to directives.
- **Role language:** answers what concrete actions should be taken.

## Architecture / Runtime / Compiler Language

### Structured Source Canon
- **Observed meaning:** underlying machine-usable source artifact, typically structured JSON/library data.
- **Implication:** remains the primary authoritative representation for compiler/runtime use.

### Rendered Reference Artifact
- **Observed meaning:** human-readable publication output such as PDF.
- **Implication:** supports review, sharing, and audit without replacing source canon.

### Role Preservation
- **Observed meaning:** rendered documentation should keep Trigger, Directive, and Instruction distinctions visible rather than flattening them.

### Hierarchy Preservation
- **Observed meaning:** document conversion must preserve category/subcategory order and structural grouping from the source.

### Auditability
- **Observed meaning:** output should remain exact enough for review and comparison against the structured source.

### Cross-Library Style Consistency
- **Observed meaning:** Trigger, Directive, and Instruction publications should follow the same formatting/template pattern.

## Definitional Candidates
- Structured source is canonical; rendered reference output is secondary.
- A library publication artifact should preserve hierarchy, exact wording, and auditability.
- Trigger, Directive, and Instruction remain distinct role libraries even when converted into shared publication format.

# BATCH-166 Compiler / Runtime Extract

## Strongest Runtime Signal
The source presents a runtime-oriented sequence:
**UMG → CEL → MUTATE → VSS → ACTIONABLE**. fileciteturn16file6

## Compiler / Runtime Issues Surfaced
1. **CEL naming conflict**
   - historical meaning noted: Creative Extension Layer
   - current runtime meaning used in-chat: Cognitive Execution Layer fileciteturn16file6

2. **Priority / merge order**
   - repo chain quoted
   - current-canon adoption not finalized fileciteturn16file6

3. **Off vs is_active**
   - `Off` treated as semantic disabled state
   - `is_active` treated as runtime activation flag
   - distinction suggested, not finalized fileciteturn16file6

4. **Schema exposure**
   - repo-style fields referenced:
     - `molt_type`
     - `label`
     - `editable_fields`
     - runtime behavior flags
     - ledger/provenance fields fileciteturn16file6

## Candidate Compiler Tasks Preserved as Evidence
- formalize handling of `Off` vs `is_active`
- formalize priority/merge order if repo chain is adopted
- expose self-describing schema fields consistently in compiler/runtime pathways fileciteturn16file6

## Stage 1 Interpretation
This batch is not a compiler spec. It is a conflict inventory for later compiler specification work.

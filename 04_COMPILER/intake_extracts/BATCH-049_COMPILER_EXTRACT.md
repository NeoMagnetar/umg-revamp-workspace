# BATCH-049 — Compiler Extract

## Compiler-Relevant Findings
- Deterministic ordering is treated as mandatory, not optional ornament.
- Validation rules are expected to reject malformed structures.
- Runtime/controller design is explicitly implied by the source, not just narrative prompting.
- Safety/bounded-agency logic belongs in enforceable runtime/controller structures.

## Concrete Compiler-Surface Candidates
- deterministic dominance ordering using effective weight + axis rank + merge rank + stable ID
- validator requiring:
  - every NeoStack has at least one NeoBlock
  - every NeoBlock has at least one MOLT atom
- overlay validation to restrict what STYLE-like overlays may modify
- RuntimeSpec compiler for ordered agency-loop execution
- Safety Layer Pack integration hooks
- audit/logging / drift threshold / bounded patch loop enforcement

## Key Risks
- source is derivative, so exact formulas and rule syntax need re-verification against canonical files
- some generated structures appear conversationally drafted rather than compiler-validated
- external governance remains under-modeled in many local sleeve descriptions

## Recommended Compiler Follow-up
1. Reconcile this batch against the canonical RuntimeSpec and Safety Layer Pack files.
2. Extract exact deterministic ordering/validation formulas from authoritative sources.
3. Add explicit governance-layer separation into the runtime schema.
4. Add continuity semantics and inter-sleeve scope validation rules.

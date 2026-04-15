# BATCH-114 — Compiler / Runtime Extract

## Stable Compiler/Runtime Boundary Signals
- UMG is pre-runtime and non-executing.
- UMG operates inside CSL.
- Execution occurs outside CSL.
- Execution systems may not:
  - mutate CSL artifacts
  - invent intent
  - bypass governance

## Determinism Requirements
- Identical blocks, structure, governance, triggers, and priorities must produce the same result.
- Silent conflict resolution is incompatible with the batch’s canon-tight framing.

## Trace / Audit Requirements
- Every outcome must explain:
  - what participated
  - what was excluded
  - why selection occurred
- If an outcome cannot be traced, it is invalid.

## Locality Constraints
### Trigger
- Eligibility gate only
- No semantic meaning
- No authority creation
- No governance bypass

### Priority
- Conflict-site only
- No semantic importance weighting
- Ignored if no conflict exists

### Governance
- Supreme
- Participation constraint only
- Pre-empts other cognition

## Runtime Terminology Note
The source records an explicit user correction:
- Use **S1+** and **S2′**
- Do not use generic System 1 / System 2 wording for UMG execution modes in canon-facing material

## Candidate Compiler / Spec Tasks
- Encode the one-page overview invariants into compiler-facing validation language.
- Ensure trace emission can explain participation, exclusion, and conflict resolution.
- Preserve execution restrictions so runtime systems cannot mutate or invent cognition.
- Reconcile earlier compiler vocabulary (for example CIR / RuntimeSpec / PCL) with the tighter overview before treating it as settled canon.

# BATCH-002 — COMPILER EXTRACT

## Scope
Compiler-specific findings extracted from the batch for later compiler audit, task specification, and parity review.

## Observed / Interpreted Public Compiler Flow
- schema and reference validation
- segment normalization
- merge handling
- bundle recording / handling
- governance application
- authority and ordering resolution
- role-based active selection
- runtime emission

## Strongest Compiler Findings
### 1. The compiler is already substantive
- This batch does not support a rewrite-from-zero framing.
- The compiler is treated as a legitimate structural system with patchable weaknesses.

### 2. Priority semantics may be globally inconsistent
- Sorting behavior, governance effects, alternates, and selector logic may not share one unified convention.
- This is treated as a foundational risk because it changes winner selection behavior.

### 3. Governance propagation may be incomplete
- Priority modification and governance effects may not propagate through all selector branches.
- `require` appears too weak if it only validates presence.
- `limit` appears insufficiently enforced during final runtime selection.

### 4. Hierarchy may be too positional
- Current structure may respect order without enforcing stronger causal gating.
- Trigger/downstream dependency semantics appear directionally desired but not yet hardened.

### 5. Primary selection may be weaker than other selectors
- Bundle/alternate rigor may differ across selector paths.
- Primary selection hardening is a likely correction target.

## Contract-First Patch Path
1. lock canonical semantics
2. define / revise compiler contract
3. patch implementations
4. compare public and private compilers
5. add parity and regression tests

## Candidate Compiler Tasks
- unify priority semantics globally
- enforce governance propagation consistently
- strengthen `require` into activation guarantee or hard failure
- enforce `limit` during actual selection
- harden primary-selection behavior
- test merges, bundles, priorities, alternates, hierarchy invariants
- verify public/private parity against one shared contract

## Confidence / Limits
- High confidence: this batch is strong on compiler concerns and sequencing logic.
- Medium confidence: broader architecture drift is plausible but not fully proven from this batch alone.
- Hard limit: private compiler behavior was not observable here.

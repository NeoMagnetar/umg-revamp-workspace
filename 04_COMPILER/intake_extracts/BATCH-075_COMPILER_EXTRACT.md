# BATCH-075_COMPILER_EXTRACT

## Scope
Compiler-adjacent and runtime-relevant material extracted from the sleeve architecture summary.

## Strong Signals
- Fusion Runtime is described as:
  - substrate draft
  - merge
  - reflection
  - final render
- Priority is expressed numerically through a weight matrix.
- Trigger events escalate weights dynamically.
- Deterministic merge types are explicitly named.
- Genesis functions as:
  - MOLT -> NeoBlock conversion surface
  - mutation engine
  - registry/version tracker
- Utility layer supports:
  - parsing
  - context stitching
  - reflection hooks
- Context injection bridges runtime and stored MOLT structures.

## Candidate Compiler Surfaces
### 1. Weight Assignment Engine
- base weight per block/layer
- escalation deltas
- dominance/override resolution

### 2. Trigger Gate Engine
- trigger detection
- internal field activation
- escalation routing

### 3. Deterministic Merge Resolver
- CORE_LOCK
- DOMINANT_FORWARD
- CONDITIONAL_ESCALATION
- STYLE_OVERLAY
- Z_AXIS_DEPTH

### 4. Genesis Factory
- MOLT -> NeoBlock conversion
- block creation/mutation interface
- version tracking
- dependency registration

### 5. Runtime Stitching Layer
- parse current inputs
- inject active context
- execute merge path
- apply reflection hook
- finalize render

## Risks
- Trigger thresholds are not numerically finalized.
- Genesis authority is broad but under-constrained.
- Spatial MOLT schema is not formalized.
- Block dependency/conflict model is incomplete.
- Weight deltas appear heuristic, not yet normalized.

## Recommended Compiler Follow-up
- isolate Genesis authority from runtime execution authority
- formalize weight precedence order
- define trigger threshold schema
- specify merge conflict rules
- map linear vs spatial MOLT handling

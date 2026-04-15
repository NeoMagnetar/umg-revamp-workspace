# BATCH-196 - Compiler Extract

## Scope
Compiler- and artifact-facing implications extracted from the canon-audit source.

## High-Value Compiler Claims
1. Compiler pipeline preserved:
   - Input: Sleeve + TriggerState
   - Output: CIR + RuntimeSpec + Trace

2. Determinism preserved:
   - same inputs -> same outputs

3. Compilation may exist in:
   - static / pre-runtime form
   - dynamic/live form

4. RuntimeSpec governs execution and executor cannot exceed it.

5. Trace records:
   - decisions
   - precedence
   - resolution steps

6. Trigger evaluation occurs externally and compiler consumes TriggerState rather than computing trigger logic itself.

## Likely Compiler Audit Targets
- formal CIR status
- TriggerState schema and lifecycle
- priority versus authority distinction
- merge block versus merge operation separation
- live compilation trigger rules
- executor obligations under RuntimeSpec
- fail-closed behavior rules

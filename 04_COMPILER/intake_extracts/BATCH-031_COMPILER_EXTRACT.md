# BATCH-031 — Compiler Extract

## Compiler-Relevant Findings
- current stack is not compiler-ready despite strong conceptual design
- trigger conditions are too lexical and prose-heavy
- bundle conditions are not normalized
- merge engine behavior is under-specified
- authority semantics are inconsistent
- exact inventory counts are missing or unreliable
- multi-block subject arbitration is unresolved
- validation-grade tests are missing

## Required Normalization Tasks
1. add canonical inventory section with exact counts for:
   - unique blocks
   - synthesized blocks
   - adapted library blocks
   - bundles
   - merges

2. normalize authority enums
   - closed enum set only
   - separate authority semantics from role precedence

3. normalize trigger logic
   - lexical candidates + classifier/pre-pass confirmation
   - detector refs instead of free prose

4. normalize bundle activation
   - machine-readable expressions over detector refs, tags, or classifier outputs

5. formalize merge engine contract
   - persistence
   - downstream reuse
   - override policy
   - dedupe
   - parent requirements
   - activation timing
   - traceability

6. add stack-level subject arbitration mode

7. add validation-grade test suite
   - trigger expectations
   - bundle activations
   - merge assertions
   - negative tests
   - ambiguity tests

## Compiler Status Signal
- recommended status now: DRAFT_ACCEPTED
- promotion target after revision: COMPILER_READY

## Related Compiler Direction
- stack “almost demands” PrePass-style activation support
- useful prepass outputs for this domain include:
  - query type
  - domain class
  - evidence level
  - explanation vs diagnosis vs prediction intent

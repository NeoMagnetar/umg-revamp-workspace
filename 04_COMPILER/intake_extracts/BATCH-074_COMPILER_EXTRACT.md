# BATCH-074 COMPILER EXTRACT

## Scope
Compiler/runtime-adjacent material surfaced across multiple documents, with the Commando Bot masterplan providing the strongest implementation signal.

## Strongest Runtime Candidates
### Commando Bot surface
- UMG preamble injected before block stack
- priority toggle system:
  - 0 off
  - 1 primary
  - 2 secondary
  - 3 tertiary
- token weighting tied to priority
- block merge engine
- payload builder
- live token estimator

### Cross-document runtime pattern
A plausible unified runtime candidate appears repeatedly:
1. parse input
2. generate context map
3. assemble active blocks
4. merge according to role/priority
5. render response
6. inject reflection / post-response review
7. adjust weights or active logic

## Compiler-Relevant Questions
- Are Commando priority + token-weight semantics implementation-specific or candidate canon?
- What is the formal ordering between role type and numeric priority?
- Is Blueprint compiled as style/control metadata or as a distinct block transform?
- Where do higher-order modules sit relative to lower-level block roles?
- What runtime surfaces are mandatory versus optional extensions?

## Intake Judgment
This is meaningful compiler evidence, but not a finalized compiler contract.
Use for audit/spec synthesis, not direct implementation lock.

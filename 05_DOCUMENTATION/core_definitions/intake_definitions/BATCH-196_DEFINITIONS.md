# BATCH-196 - Definitions Extract

## Terminology Scope Note
These definitions are extracted from a derived canon-audit summary.
They remain Stage 1 evidence until explicitly promoted elsewhere.

## Core Terms
Cognitive Specification Layer
Non-executing cognition jurisdiction or specification layer that defines cognition structurally while leaving execution external.

CIR
Compiled intermediate artifact preserved in the source as one layer in the artifact model between sleeve/trigger inputs and executor-facing RuntimeSpec.

RuntimeSpec
Executor contract produced by deterministic compilation. It governs execution and is not equivalent to cognition construction itself.

Decision Trace
Audit artifact recording precedence, decisions, and resolution steps taken during compilation.

## Additional Structural Terms
Merge Block
Block carrying must-include content or constraints, additive in nature.

Merge Operation
Compiler/synthesis operation distinct from Merge Block.

FAIL_CLOSED
Safety stance in which invalid states halt rather than degrade silently.

## Definitional Candidates
- Governance occurs before execution.
- RuntimeSpec governs execution; executor does not modify cognition.
- Safety is encoded structurally, not reactively.

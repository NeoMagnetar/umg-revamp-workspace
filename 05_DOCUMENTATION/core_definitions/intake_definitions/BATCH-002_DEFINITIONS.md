# BATCH-002 — DEFINITIONS EXTRACT

## Terminology
### Compiler
A deterministic structural engine that compiles sleeve-like JSON into runtime-facing artifacts. In this batch it is explicitly not treated as a reasoning engine.

### Structural compilation
The compiler behavior described in the batch: validate, normalize, merge, apply governance, resolve active content, and emit runtime artifacts.

### Compiler contract
The defined semantic and operational rules the compiler is supposed to implement. This batch argues that the contract should be stabilized before patching code.

### Public compiler
The accessible `umg-compiler` build reviewed in the batch. It is the visible evidence surface for current implementation analysis.

### Private compiler
The Replit / UMG Studio compiler mentioned as expected to match public behavior, but not visible in this batch.

## Role Language
### MOLT
The classic visible seven-role taxonomy referenced in the batch:
- Trigger
- Directive
- Instruction
- Subject
- Primary
- Philosophy
- Blueprint

### Trigger
A visible classic MOLT role. The batch suggests future stronger downstream gating may be needed, but does not treat that as already implemented.

### Primary
A visible classic MOLT role. The batch flags primary selection logic as possibly weaker than other selector paths.

### Blueprint
A visible classic MOLT role associated with output-facing emission, but still downstream of structural compilation.

## Architecture Language
### Hierarchy
The ordering and/or dependency structure between UMG units. This batch argues current implementation may follow hierarchy more as ordered structure than as strong dependency-enforced semantics.

### Pre-pass
A possible stage mentioned directionally in broader UMG evolution. In this batch it is unresolved whether pre-pass is a compiler-native stage, runtime stage, or both.

### NeoBlock
A runtime-facing emitted unit discussed as compiler output. No new taxonomy is finalized here.

### NeoStack
A runtime-facing stack structure discussed as compiler output. No new architecture is finalized here.

## Runtime / Compiler Language
### Governance
Structural control behavior applied before final selection. The batch references forbid / require / prefer style behavior and flags inconsistency in propagation and guarantees.

### Require
A governance mode that, in this batch, appears too weak if it only validates existence rather than ensuring meaningful activation or hard failure.

### Limit
A governance or selector constraint described as potentially nominal if not enforced during actual runtime selection.

### Priority
A selection-strength or ordering signal. This batch treats it as a major defect area because different parts of the compiler may not be using one unified convention.

### Merge
A deterministic compile-phase structural substitution or combination step. The batch does not treat current merge behavior as deep semantic synthesis.

### Bundle
A grouping and downstream selection structure. The batch suggests bundle containment and selector rigor may be uneven across paths.

## Definitional Candidates
- The compiler is a deterministic structural engine, not a reasoning engine.
- Canonical semantics should be stabilized before compiler patching.
- Hierarchy may need to be defined as stronger dependency-enforced semantics, not only positional order.
- Public/private compiler parity should be evaluated against one shared semantic contract.

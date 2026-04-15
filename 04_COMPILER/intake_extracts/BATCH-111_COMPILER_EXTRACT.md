# BATCH-111 — Compiler Extract

## Compiler-Sensitive Findings
- A surfaced warning document contributes concrete runtime/compiler diagnostics vocabulary.
- Example signals include:
  - unused trigger
  - skipped governance rule
  - soft governance override
  - directive conflict resolved
  - instruction conflict resolved
  - multiple primary candidates
  - redundant bundle
  - unused bundle/merge segment
  - governance conflict
- A surfaced snippet also includes structured trace/compile shapes such as `TraceEvent` and `CompileResult`.

## Proposed Compiler/Runtime Flow Present in This Batch
1. Parse
2. Validate
3. Assemble
4. Emit runtime + trace

## Candidate Compiler Work Surfaced Here
- parser
- merge engine
- governance resolver
- trace generator
- future compile / validate / trace endpoints for MCP-style exposure

## Diagnostics / Schema Pressure
- Treat the warning/error vocabulary as a tracked schema candidate rather than casual prose.
- Preserve explicit links among:
  - MOLT hierarchy
  - governance
  - triggers
  - bundles / merges
  - runtime assembly
- Runtime warnings should be auditable, structured, and attachable to trace output.

## Candidate Compiler Tasks
- Extract formal trace/event schemas from the warning vocabulary source.
- Define conflict diagnostics for:
  - directives
  - instructions
  - multiple primary candidates
  - unused triggers
  - redundant bundles
  - governance conflicts
- Preserve separate compile stages for parsing, validation, assembly, and runtime/trace emission.

## Risk Note
This batch surfaces promising compiler structure, but most of it remains planning language rather than finalized compiler canon. Keep diagnostics extraction separate from broader app-stack proposals.

# BATCH-007 — Compiler Extract
## Compiler / Runtime-Relevant Signals
- The batch does not redesign the compiler directly, but it identifies missing anchor artifacts that cause messy system-check behavior.
- Proposed anchor files include a base sleeve file, MOLT map schema, tag semantics file, process-law file, and explicit system-check protocol.
- System/runtime checks should reference those artifacts explicitly rather than improvising around their absence.
- Missing-anchor conditions should be treated as structural validation failures, not silently patched over by ambiguous behavior.
- NL-first stabilization is preferred before CyentCore compression or deeper syntax/compiler mapping.

## Candidate Compiler / Runtime Tasks
- Add missing-anchor validation for:
  - base sleeve anchor
  - MOLT map schema
  - tag semantics
  - system-check protocol
- Make system checks explicitly reference those artifacts.
- Preserve the distinction between validation and permission.
- Preserve the distinction between inspection and execution.
- Support a neutral governed base sleeve as the default host state for explicit mode activation.

## Compiler Caution
This batch is mostly topology and artifact hygiene, not a finalized compiler rewrite. The main value is defining prerequisites for cleaner runtime behavior and cleaner checks.

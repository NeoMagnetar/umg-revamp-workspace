# BATCH-197 - Compiler Extract

## Scope
Compiler- and toolchain-facing implications extracted from the language-layer source.

## High-Value Compiler Claims
1. Proposed toolchain components include:
   - parser
   - validator
   - transpiler
   - runtime library
   - CLI
2. Proposed CLI commands include:
   - `umg init`
   - `umg dev`
   - `umg build`
3. Proposed compiler/emitter direction includes:
   - HTML/CSS/JS bundles
   - React / Vue / Svelte emitters
4. Proposed later experimental backend bridge includes:
   - Express / FastAPI endpoint generation from Instruction blocks
   - shared service contracts across front and back
5. Strong caution preserved:
   - these roadmap/tooling claims were later acknowledged as strategic rather than fully audited

## Likely Compiler Audit Targets
- whether NeoCore JSON Schema v1 should be frozen first
- actual maturity of parser/validator/transpiler/runtime assets
- frontend-first scope versus backend expansion
- source-to-schema translation rules among Cantocore, Cyentocore, and NeoCore
- examples/docs/playground requirements for launch

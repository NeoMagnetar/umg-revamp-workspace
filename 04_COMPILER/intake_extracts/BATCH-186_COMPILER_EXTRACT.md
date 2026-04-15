# BATCH-186 - Compiler Extract

## Scope
Compiler- and runtime-facing implications extracted from the education-facing source.

## High-Value Compiler Claims
1. The source treats hierarchy as execution priority, not just conceptual layering.
2. The only directly confirmed priority facts in this chat are:
   - Trigger first
   - Directive next
3. Formula-based generation implies a runtime flow:
   - choose blocks
   - arrange them in priority order
   - apply them to generation
4. Public-facing explanation must not outrun canonical runtime precedence.
5. Educational stack explanations need a canon-faithful mapping to actual runtime order.

## Likely Compiler Audit Targets
- public-safe hierarchy language
- verified full priority chain for block types
- separation between educator explanation and compiler mechanics
- classroom formula examples that do not misstate runtime order

# BATCH-171 Compiler Extract

## Compiler / Runtime Candidate Surfaces
- trigger matching library
- directive-set planner
- instruction layer resolver
- overlay pre/post hooks
- merge collision resolver
- hard-constraint gate
- audit path recorder

## Candidate Runtime Rules
1. Match events against trigger conditions.
2. Sort trigger results by priority.
3. Activate directive sets.
4. Resolve instruction layers attached to those directives.
5. Run overlays around execution.
6. Merge output into state after each layer.
7. If hard constraints fail, block output and route into conflict resolution.
8. Record audit events, conflicts, overlays, path, and latency.

## Notable Candidate Semantics
- runtime is hybrid, not fully simultaneous or fully serial
- bounded parallelism is queue-based
- state collisions should prefer higher producer weight or higher directive priority
- conflict routing is an engine behavior, not manual patchwork

## Caution
These are implementation proposals extracted from the chat, not ratified UMG runtime canon.

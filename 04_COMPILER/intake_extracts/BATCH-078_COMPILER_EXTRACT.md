# BATCH-078 Compiler Extract

## Scope
Compiler/runtime-adjacent material in the NeoUMG AI Framework handoff summary.

## Strong Signals
- Priority is treated as a formal runtime control field, not just descriptive metadata.
- Stack parsing is explicitly connected to execution behavior and routing signals.
- Merge is expected to surface incompatibility rather than hide it.
- Reflection appears as a runtime feedback/evaluation loop.
- Export/import schema and builder metadata are treated as part of the compiler surface.

## Candidate Runtime Flow
1. Parse active UMG stack.
2. Read typed blocks and priorities.
3. Convert block roles into runtime signals.
4. Apply role- and priority-conditioned routing/activation logic.
5. Perform merge/conflict checking.
6. Compose prompt / runtime representation.
7. Optionally score/reflect and feed back into later runs.

## Candidate Fields Affecting Compilation
- `type`
- `content`
- `priority`
- `cantocore`
- `id`
- `created_at`

## WINA Mapping Pressure
The source proposes a concrete but still conceptual bridge from semantic block priorities to sparse activation budgets and neuron-importance modulation. This is high-value compiler evidence, but it remains design input rather than validated implementation.

## Candidate Tasks
- formal parser for typed block stacks
- deterministic prompt composer
- conflict-aware merge logic
- export/import schema validator
- priority-to-runtime mapping rules
- reflection feedback handling
- adapter surface for routing/sparsity experiments

## Cautions
- WINA integration is conceptual in this source.
- Priority semantics may drift if not normalized against earlier batches.
- Trigger and Bundle remain underdefined compared with stack, merge, and priority.

Source basis: uploaded handoff summary on NeoUMG AI Framework. See fileciteturn13file0

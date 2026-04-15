# BATCH-169 — Sleeve Extract

## Why this extract exists
This source contains concrete sleeve-loading and active-state handling details, not just abstract sleeve references. fileciteturn19file0

## Preserved Sleeve Evidence
Referenced runtime files:
- `SLEEVE.ANALYST.json`
- `SLEEVE.CODER.json`
- `SLEEVESTACK.DEFAULT.json`

## Preserved Runtime Handling
- unify sleeve loading in `src/sleeve_manager.py`
- copy full sleeve JSON into `memory/active_state.json`
- remove duplicate or partial loader behavior from `agent_commands.py`
- repair `command_registry.json` so runtime calls point to real callable logic. fileciteturn19file0

## Why it matters
This batch turns sleeve handling into an implementation issue:
- one loader should be authoritative
- active sleeve state should be complete, not just an ID
- sleeve switching should be stable and inspectable
- duplicate/partial runtime paths are a reliability risk

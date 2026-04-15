# BATCH-013_NEOSTRUCTURE_EXTRACT

## NeoStack Architecture
### Tri-State Availability
- `OFF` = unavailable; cannot self-enable
- `ON` = available and usable
- `ADAPTIVE` = available; assistant may locally toggle if policy permits

### Locked Stacks
- Visible
- not toggleable at runtime by assistant or user within the chat session

## NeoBlock Behavior
- NeoBlocks may be created at runtime inside allowed stacks
- must pass validation
- remain session-local unless promoted

## Reconfiguration Stack
- `NSTK.BlockReconfig.v1` introduced as a bounded mutation stack
- intended to support controlled creation, merge, bundle, and reconfiguration work

## Snapshot Guidance
- Active structures should be represented through real registries
- quick-reference snapshots should show real NeoBlocks with short descriptions

# BATCH-104_BLOCKS_MOLT_EXTRACT

## Scope
MOLT / block-role / candidate-block signals extracted from BATCH-104.

## MOLT / State Signal
The source associates Context & State with MOLT-like state mapping and treats this as the explicit, legible store for:
- current situation
- historical continuity
- active constraints
- agent state

This matters because it keeps state representation visible rather than hidden in latent activations.

## Candidate Block Families
The batch names several candidate block surfaces:
- **WorldModelBlocks**
- **PredictiveBlocks / StateMaps**
- **Planning & Action Blocks**
- **Governance Blocks**
- **Memory / MOLT Blocks**

These are useful because they imply clearer functional separation rather than blended cognition/action blocks.

## Composition Signal
- World-model outputs do not directly execute.
- Predictive layers merge into broader system state or planning inputs.
- Governance and memory/state layers remain separate responsibilities.
- Planning/action blocks appear downstream of simulation and constraint checking.

## Boundary Pressure
This batch strongly pressures clarification of:
- whether PredictiveBlocks and WorldModelBlocks are the same class or different classes
- whether MOLT state maps are storage surfaces, interpretation surfaces, or both
- how planning consumes state and simulation results without role overlap

## High-Value Documentation Targets
- preserve world model as subordinate subsystem rather than cognitive totality
- document MOLT/state as explicit legible context layer
- clarify WorldModelBlock versus PredictiveBlock naming and responsibilities
- show how planning/action blocks consume governed state rather than raw prediction

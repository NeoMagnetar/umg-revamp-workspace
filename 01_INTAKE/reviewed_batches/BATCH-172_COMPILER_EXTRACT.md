# BATCH-172 Compiler / Runtime Extract

## Runtime-Relevant Signal
The batch implies several runtime-definition needs without resolving them:

1. Portable personality package definition
   - what fields must exist
   - how behavior state is represented
   - how portability works across model backends

2. Cross-model execution behavior
   - how personality/behavior blocks are applied consistently
   - how governance and visual transparency survive backend differences

3. Real-time behavior control
   - what runtime surfaces are observable
   - what controls are user-facing
   - how auditability is represented technically

4. Integration-layer execution
   - UMG as a personality or behavior plugin on top of external agent frameworks

## Evidence Classification
These are compiler/runtime pressures, not finalized specs.

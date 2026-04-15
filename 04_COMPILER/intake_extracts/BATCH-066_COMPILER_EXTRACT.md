# BATCH-066 Compiler Extract

## Compiler-relevant signals
- Merge app-level roles into executable services:
  - Primary
  - Merge
  - Blueprint
  - Overlay
  - Instruction
  - Trigger
  - Meta / Reflective
- Support threshold-gated action:
  - execute only if confidence exceeds threshold
  - require user approval for larger trades
- Support event triggers:
  - trend spike
  - news spike
  - transcript/upload arrival
  - price divergence after event
  - periodic heartbeat loop
- Support shared-vault coordination for multi-agent systems
- Support explainable logging and snapshots for each decision

## Runtime patterns worth formalizing
1. **Immutable kernel load**
   - load aligned core and hard constraints
2. **Overlay attach**
   - attach strategy philosophy and context layers
3. **Instruction attach**
   - apply task/risk/entry/exit modules
4. **Meta tune**
   - apply subtle bias adjustments
5. **Trigger evaluation**
   - detect events, thresholds, and update conditions
6. **Shared-vault sync**
   - write conflict logs, state, and decision traces
7. **Action gate**
   - allow analysis/alert/trade only under permissions and thresholds
8. **Post-action reflection**
   - reflect post-trade or post-alert

## Candidate compiler tasks
- formalize shared-vault tether protocol
- formalize async convergence and 2-of-3 agent confirmation rules
- formalize relevance scoring and threshold-based notifications
- formalize rendering-surface independence from underlying block logic

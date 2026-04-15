# BATCH-093 Compiler Extract

## Scope
Compiler/runtime-relevant signals extracted from the batch.

## High-Signal Runtime Claims
- Load order is described as:
  1. core vault
  2. project vault
  3. instruction embed
  4. input processing as MOLT
- Stack operations include add, merge, and prioritize.
- Reflection loop detects change, evaluates merge, and updates the stack.
- Trigger blocks can activate persistence or conflict-resolution behaviors.

## Candidate Compiler Surfaces
### Loader / Intake
- Support loading multiple vault bundles into one runtime stack.
- Preserve distinction between core/global bundles and project/context bundles.

### Typing / Routing
- Support typed block routing via explicit type declarations.
- Handle core and extended role surfaces without silently collapsing them.

### Merge Logic
- Gate merge on stronger/superior logic checks.
- Preserve clash-resolution step rather than unconditional overwrite.
- Consider philosophy-layer influence during merge conflict resolution.

### Priority Logic
- Allow recency/frequency weighting as one prioritization signal.
- Keep this separate from canonical semantic priority unless later approved.

### Trigger Logic
- Model trigger expressions as event-conditioned behavior activators.
- Candidate surfaces include user-command triggers, conflict triggers, and change-detection triggers.

### Reflection / Update
- Detect change events.
- Run evaluation before updating.
- Preserve user-controlled persistence boundary; runtime reflection is not the same as autonomous write authority.

## Risks
- The source is a summary, not implementation evidence.
- CantoCore grammar is informal/evolving; parser commitments would be premature.
- Extended taxonomy may not yet be canonical.
- Blend between architecture semantics and deployment convenience remains unresolved.

## Recommended Compiler Decision Target
Decide whether the compiler should formally recognize:
- vault bundle loading
- typed extended block roles
- trigger grammar
- superiority-gated merge/update
or whether these remain provisional runtime conventions until semantic alignment is complete.

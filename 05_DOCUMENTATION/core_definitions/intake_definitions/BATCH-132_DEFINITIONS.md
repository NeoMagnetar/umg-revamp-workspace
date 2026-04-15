# BATCH-132 — Definitions Extract

## Terminology Scope Note
These definitions are extracted from a derived showcase and release-path summary.
They remain Stage 1 evidence until explicitly promoted elsewhere.

## Public Demo and Product Terms
**Compile-Only Mode**  
Public-facing mode where users can author blocks and inspect compiled RuntimeSpec and Trace without consuming live model inference.

**Generate Mode**  
Downstream inference step that uses compiled artifacts to produce model output.

**BYOK**  
Bring Your Own Key access model in which users supply their own API credentials for generation.

**Hybrid Quota + BYOK**  
Release model offering limited owner-funded runs for initial demo use, with heavier usage shifting to user-supplied keys.

## Compiler-to-Runtime Terms
**RuntimeSpec**  
Compiled artifact describing what will happen or what is active for downstream use.

**Trace**  
Forensic record explaining why the result happened and how it was derived.

**Deterministic Serializer**  
Proposed adapter that translates RuntimeSpec into model-ready input without collapsing UMG back into ad hoc prompt engineering.

**RuntimeSpec Hash**  
Canonical runtime fingerprint proposed as the key for caching and replay behavior.

## Demo Architecture Terms
**Blocks → Compiler → RuntimeSpec + Trace → Response**  
Public-facing explanation of UMG as a real system layer rather than a prompt wrapper.

**A/B Cognition Demo**  
Suggested showcase that compares UMG-mode compiled behavior against a flat-prompt baseline.

**Governance Conflict Demo**  
Suggested signature showcase where colliding instructions are resolved visibly through governance and Trace.

## Definitional Candidates
UMG should be shown as a cognitive spec layer, not a prompt builder.  
Blocks → compiler → RuntimeSpec + Trace → response.  
You’re not prompt engineering, you’re serializing a spec.

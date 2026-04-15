# BATCH-142 — Compiler Extract

## Scope
Compiler- and export-facing implications extracted from the bot-maker taxonomy source.

## High-Value Compiler Claims
1. Builder selections should be transformable into a normalized `agent_profile.json` or equivalent export artifact.
2. Human-readable descriptors should be normalized into structured namespace tags where logic/filtering/export behavior is needed.
3. Compatibility/conflict checks are needed for combinable traits, tone, motivation, overlays, and other layered elements.
4. Programmable traits should be preferred over flavor-only traits when runtime behavior is expected.
5. Safety/control configuration should be a separate builder/configuration layer rather than hidden inside personality.
6. Export targets imply a later compile step from wizard selections into profile, preview, zip, or deployable folder artifacts.

## Likely Compiler Audit Targets
Tag namespace normalization.
Trait compatibility/conflict rules.
Selection-to-profile transformation.
Profile schema for `agent_profile.json`.
Boundary between descriptive labels and runtime-usable tags.
Safety/control layer separation from personality layers.

## Risk Surface
Any builder that treats descriptive labels as already sufficient runtime logic would conflict with this batch’s strongest distinction.
Any product flow that mixes capability, safety, memory, and personality into one undifferentiated layer would weaken the builder architecture surfaced here.

# BATCH-084 — Blocks / MOLT Extract

## Scope
This extract captures role/taxonomy surfaces that are explicit in the batch.

## Explicit Role Set
- Primary
- Subject
- Philosophy
- Instruction
- Merge
- Overlay (appears once in a flat loadout snapshot, but not sustained)

## Example Runtime Loadout
- Primary = PROD.MODEL.RUN
- Subject = UMG_FRAMEWORK_DEPLOYMENT
- Philosophy = ALIGNMENT>UTILITY; SELF-CHECK=ON
- Instruction = MERGE_PRIORITY=LOGIC; BLOCK_EXECUTION=RECURSIVE
- Overlay = NONE

## Example CyentCore / CantoCore-style Block Set
- Primary: PROD.MODEL.RUN; SCOPE=UMG.REALITY.CORE; MODE=MULTI_AGENT
- Subject: ROUTING=GPT4|CLAUDE|GEMINI|MISTRAL; RAG=QDRANT
- Instruction: CHECKLIST=UNDERSTAND>REFLECT>REFINE; FALLBACK=INJECT.REFLECT.BLOCK; STATUS_BADGES=ON
- Philosophy: ALIGNMENT>UTILITY; TRANSPARENCY=HUD.ON; PRIVACY=MPC|ZK.TOGGLE
- Merge: TASKS=[REPORTS, TRADER, MEDIA, VR]; UI=MIND.HUD; MEMORY=MEC

## Role Reading
This batch treats MOLT roles as runtime-executable controls rather than only semantic documentation categories. The most important pressure is that these roles now map directly to:
- routing
- fallback
- privacy
- alignment
- task scope
- memory and HUD surfaces

## Stability Notes
- Overlay appears but is not sustained enough to be treated as stabilized.
- NeoBlock / NeoStack / Sleeve are not strongly advanced here.
- The role system is implementation-facing, but still provisional in its broader normalization.

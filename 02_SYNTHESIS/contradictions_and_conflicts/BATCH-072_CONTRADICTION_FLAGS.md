# BATCH-072 Contradiction / Ambiguity Flags

## Flag 1 — Provenance Folder Naming
- Competing names appeared:
  - `meta/`
  - `vault/`
  - `meta-vault/`
- The source says preference leaned toward `meta-vault/`, but the naming was not fully stabilized.

## Flag 2 — README vs Folder Semantics
- Repeated confusion existed around whether adding `README.md` inside `meta-vault/` would preserve the folder as a folder.
- This is not a deep doctrinal contradiction, but it signals implementation/documentation ambiguity.

## Flag 3 — Lexicon vs Glossary vs System Terms
- The distinction was refined live rather than fixed from the start.
- Editorial cleanup is still likely needed before these categories can be treated as stable documentation boundaries.

## Flag 4 — Trigger Reliability
- Audit triggers were named and saved, but the source also reports that some prior chats understood the JSON audit request and some did not.
- This creates a gap between intended trigger semantics and observed behavior.

## Flag 5 — STAK Status
- STAK is described as a reusable per-chat audit structure, but the source does not settle whether it is:
  - a documentation artifact
  - a runtime stack
  - a storage record
  - all of the above

## Flag 6 — Audit Layer vs Core UMG Layer
- The batch strongly contributes to UMG operations, but it is still unclear whether these concepts belong to:
  - core UMG semantics
  - documentation infrastructure
  - skill infrastructure
  - compiler-adjacent tooling

## Recommended Handling
Treat all six flags as synthesis-stage clarification targets. None of them should be silently flattened in Stage 1.

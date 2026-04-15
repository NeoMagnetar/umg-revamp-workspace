# BATCH-160 — Sleeve Extract

## Sleeve / resleeving findings
- Sleeves are treated as first-class structured runtime objects rather than informal style prompts.
- Proposed sleeve spec preserves:
  - `id`
  - `overlays`
  - `style`
  - `caps`
- Sleeves are described as:
  - personas / overlays
  - runtime behavior packs
  - switchable identity layers
- The target runtime should support sleeve swapping without alignment drift.
- Runtime logic implies:
  - versioned sleeve files
  - middleware injection of current sleeve before each call
  - overlay-aware operation
  - promotion artifacts tied to sleeve versioning

## Candidate runtime role
Sleeves appear as modular identity/runtime layers that should remain configurable and swappable while staying subordinate to the Alignment Spine.

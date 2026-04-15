# BATCH-175 — Contradiction Flags

## Purpose
Track tensions and unresolved terminology without silently harmonizing them.

## Flag 1 — `stack` Overload
### Evidence
The batch uses `stack` in two incompatible senses:
1. strict compiler meaning: same-type priority resolution
2. everyday layered grouping meaning: personality stack, business stack, tech stack, etc.

### Risk
This can produce semantic drift across docs, compiler descriptions, UI, and user-facing language.

### Stage 1 Handling
Preserve explicitly. Do not normalize away.

---

## Flag 2 — Human-Facing Grouping Term Not Settled
### Evidence
The batch explores `domain`, `profile`, `bundle`, `preset`, and rejects or questions some of them.

### Risk
Cross-type grouping language could fork documentation and implementation narratives.

### Stage 1 Handling
Mark unresolved. Route to semantic review.

---

## Flag 3 — Snap Semantics Previously Overloaded
### Evidence
The source notes repeated refinement to keep snap from drifting toward merge/grouping/hierarchy meanings.

### Risk
Compiler logic and documentation may diverge if snap remains semantically loose.

### Stage 1 Handling
Keep as explicit ambiguity until fixed in decision process.

---

## Flag 4 — UI Richness vs Canon Restraint
### Evidence
The batch explores graph/UI models that are not yet canonically formalized.

### Risk
Visual mental models may back-propagate into semantic rules.

### Stage 1 Handling
Treat UI ideas as non-canon until separately specified.

## Disposition
Contradictions preserved for later synthesis and decisions review.

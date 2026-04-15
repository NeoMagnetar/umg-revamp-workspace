# BATCH-108 — Project Impact Map

## Primary domain
Builder graph semantics, runtime interaction model, and stack behavior.

## Roadmap phases touched
- PHASE_1_CORE_ALIGNMENT
- PHASE_2_COMPILER_IMPACT
- PHASE_3_DOCUMENTATION_IMPACT
- PHASE_4_SKILL_ALIGNMENT
- PHASE_5_PRD_AND_STAGING

## Contradiction watch
HIGH

### Main contradiction / tension points
1. **Graph freedom vs UMG hierarchy**
   - Generic graph tooling invites unconstrained node placement.
   - UMG semantics require rooted, ordered structure.

2. **`Deployment` in builder taxonomy**
   - Present in this builder-facing packet.
   - Elsewhere in intake stream, `Deployment` has been questioned as a main MOLT role.

3. **Merge UX not finalized**
   - Auto-merge by horizontal placement versus explicit merge confirmation remains open.

4. **Current codebase state unclear**
   - Some plans predate the shared advanced `GraphCanvas.tsx`, so older implementation advice may now be partially stale.

## Duplicate pressure
YES

### Likely overlaps
- Builder schema and recovery packets
- Graph/runtime staging packets
- Role taxonomy packets
- Stack / merge semantics packets

## Likely downstream targets
- `04_COMPILER`
- `05_DOCUMENTATION/blocks_and_molt`
- Builder UI spec / PRD staging materials
- Future graph-canvas implementation work
- Skill alignment for builder-facing tools

## Next decision target
Whether the canonical builder rule set is:
- always start with Primary
- never allow placement above Primary
- vertical = stack priority
- horizontal = overlay / merge attempt

and whether this becomes a stable control rule for all builder implementations.

# BATCH-108 — Compiler / Runtime Extract

## Main runtime claims
- Builder runtime should load manifests by plan type.
- Builder runtime should load block JSON by path.
- Blocks should render as nodes with UMG-specific constraints.
- Generic graph behavior must be restricted by UMG stack semantics.

## Candidate runtime components
- `GraphCanvas.tsx`
- `flowUtils.ts`
- `snapLogic.ts`
- `mergeEngine.ts`
- `BlockNode.tsx`
- `StackColumnGuide.tsx`
- `ZoomControls.tsx`

## Candidate functions
```ts
canMerge(target, incoming)
mergeBlocks(target, incoming)
```

## Candidate interaction rules
1. Always start with a Primary block.
2. Reject placements above Primary.
3. Dropping below a block/root:
   - create or extend a vertical stack
   - update stack priority
4. Dropping beside a block:
   - attempt overlay / merge if allowed
5. Save/load must preserve:
   - stack order
   - stack grouping
   - overlay/merge semantics

## Candidate compiler/runtime tasks
- Encode stack priority into node layout and restoration logic.
- Distinguish vertical snap vs horizontal merge in drag/drop handling.
- Preserve merged-state metadata for later editing / undo.
- Support new stack creation when dropping into blank canvas space.
- Keep graph freedom subordinate to semantic hierarchy.

## Runtime risks exposed
- Graph regressions can erase block movement / interaction.
- Generic graph tooling may weaken or erase Primary-root rules.
- Merge semantics remain underdefined compared with stack semantics.
- Current codebase state may already exceed earlier planning assumptions, requiring patching rather than greenfield implementation.

## Implementation disposition
Treat as high-value implementation evidence, not finalized compiler spec.

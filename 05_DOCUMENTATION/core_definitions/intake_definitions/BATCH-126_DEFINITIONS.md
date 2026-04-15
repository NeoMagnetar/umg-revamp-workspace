# BATCH-126 — Definitions Extract

## Terminology Scope Note
These definitions are extracted from a derived summary source.
They remain Stage 1 evidence until explicitly promoted elsewhere.

## Core System Terms
**Block**  
The modular unit underlying all UMG composition. Larger structures may be compressed assemblies of blocks.

**Column / MOLT Column / cocoon**  
A vertically organized structural unit associated with MOLT ordering. The source indicates terminology is still somewhat fluid here.

**NeoBlock**  
A compressed representation of one Column that should preserve provenance and expose one MOLT type upward in v0.

**NeoStack**  
A grouping of 2+ snapped sibling NeoBlocks that belong together without themselves being an authority or precedence layer.

**Sleeve**  
The top-level organism and compiler input containing all internal composites.

## Authority and Resolution Terms
**MOLT**  
Treated in this source as the fixed hierarchy of authority, with the order Trigger, Directive, Instruction, Subject, Primary, Philosophy, Blueprint.

**priority_group**  
Categorical priority system replacing `stack_rank`, used only among peers in the same scope and resolution context.

**Bundle**  
Mode where multiple contributions remain active and priority orders influence without compile-time elimination.

**Merge**  
Operation used when multiple contributions must become one outcome, as structured assembly or explicit typed combination rather than untyped fusion.

**Synthesis**  
Explicit, traceable resolution stage distinct from raw structure and distinct from bundle/merge as mere UI adjacency.

**Attachment**  
Defines scope of application rather than authority. Attachment does not alter a block's MOLT identity.

**Governance**  
Explicit, scoped, traceable control layer treated here as useful but not strictly required. Exact semantics remain partly unsettled.

## Runtime / Compiler Terms
**RuntimeSpec**  
Compiled output of the compiler representing resolved active structure.

**Trace**  
Mandatory forensic record of validation, bindings, off-state removals, bundle ordering, merge decisions, synthesis provenance, runtime build, and final hash.

**Canonicalization**  
Normalization process used to produce stable, reproducible compiler output.

**Stable Hash**  
Expected reproducible hash of canonicalized RuntimeSpec for auditability and determinism.

## UI / Rendering Terms
**Zoom Levels**  
Different views of the same underlying structure, from Sleeve down to raw blocks, without semantic change.

**UI Semantics Mapping**  
Design principle that UI gestures must emit explicit metadata and may not silently create compiler meaning.

## Definitional Candidates
Everything is a block; some blocks are larger because they are compressed assemblies of other blocks.  
MOLT decides who is allowed to win; priority decides which one wins when the same kind collide.  
Bundle uses priority to order influence; merge uses priority to resolve conflict.  
Block attachment defines scope of application, not authority.  
The compiler takes a Sleeve and deterministically emits RuntimeSpec plus Trace.

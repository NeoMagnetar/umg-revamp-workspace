# BATCH-131 — Definitions Extract

## Terminology Scope Note
These definitions are extracted from a derived Studio v1 product-spec summary.
They remain Stage 1 evidence until explicitly promoted elsewhere.

## Core Studio Terms
**Active Sleeve**  
The single working document loaded, edited, compiled, saved, and exported in Studio.

**Graph / Matrix**  
Spatial reflection of structure used for overview, arrangement, and selection; not the source of semantic truth.

**Bottom Panel**  
Primary mutation surface for editing and composition operations.

**Right Panel**  
Compiler input/output, diagnostics, governance editing, block inspection, and controlled JSON apply/revert surface.

## Structural Authoring Terms
**MOLT Column**  
A vertical ordered set of blocks in canonical MOLT lanes intended to become a NeoBlock.

**Lane**  
Visual/type-specific position for a block; movement within a lane changes order but not type.

**Compress**  
Structural packaging step that converts exactly one active column into one NeoBlock.

**NeoBlock**  
Compressed representation of exactly one MOLT column in Studio v1.

**NeoStack**  
Grouping of multiple NeoBlocks within a Sleeve; peer-conflict scope for v1 governance.

## Composition Terms
**Bundle (v1)**  
Same-MOLT-only operation that preserves multiple blocks as an ordered internal group while replacing them with one composite result in structure.

**Merge (v1)**  
Same-MOLT-only explicit operation that synthesizes a new composite block, with provenance preserved internally.

**Anchor**  
First selected block in a merge flow; determines resulting MOLT type.

## Control and Ordering Terms
**Priority Tag**  
Normal preference indicator with values High, Medium, or Low.

**Rank / Order**  
Relative position within a lane or grouped structure.

**Governance Override**  
Scoped law-level conflict resolution above normal priority within a NeoStack.

**Compile Status**  
Explicit Studio state values including Idle, Dirty, Compiling, Compiled OK, Compiled Warnings, and Compile Failed.

## Persistence Terms
**Compiled Sleeve File Format**  
Portable Studio artifact containing format identity, compiler metadata, sleeve, layout, compile outputs, and hashes.

**Layout Metadata**  
Studio/UI information stored with the Sleeve artifact but excluded from compiler semantics.

## Definitional Candidates
All semantic editing occurs within exactly one MOLT column at a time.  
Graph is the map, not the engine.  
Priority is opinion. Governance is law.  
You do not edit the graph. You work on one MOLT stack (column) at a time. Everything else is arrangement of completed units.

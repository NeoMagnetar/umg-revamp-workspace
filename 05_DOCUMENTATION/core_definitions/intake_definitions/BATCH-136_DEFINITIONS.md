# BATCH-136 — Definitions Extract

## Terminology Scope Note
These definitions are extracted from a raw block artifact.
They remain Stage 1 evidence until explicitly promoted elsewhere.

## Core Artifact Terms
**Instruction Block**  
A block whose primary function is to encode procedural rules, operational logic, or bounded task instructions.

**CantoCore Payload**  
The main terse rule body of the block, here used to express SemVer logic in compressed instruction form.

**Editable Fields**  
Declared fields that the authoring environment may allow to be directly modified.

**Example Block Data**  
Illustrative applied example attached to the block without changing the block’s semantic role.

## Block-Schema Terms Present in Source
**block_id**  
Persistent identifier for the block.

**label**  
Human-facing name for the block.

**category**  
Domain grouping label, here `Software.Versioning`.

**molt_type**  
Declared role category, here `Instruction`.

**tags**  
Auxiliary domain labels for search or organization.

**ledger**  
Provenance/accountability metadata including originator, verification, timestamps, and edit log.

**display**  
Renderer-facing metadata such as color and icon.

**snap_config**  
Likely UI/layout relationship setting rather than semantic law.

**merge_logic**  
Block-declared interaction hint requiring canon review.

## Definitional Candidates
A role-pure Instruction block should encode method, rule, or procedure rather than worldview or output style.  
Outer block metadata should be separated into semantic, compiler, and renderer/persistence layers.  
Example data may illustrate application without redefining the block itself.

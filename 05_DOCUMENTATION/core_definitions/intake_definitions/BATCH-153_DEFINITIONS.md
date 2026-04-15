# BATCH-153 — Definitions Extract

## Terminology Scope Note
These definitions are extracted from a derived minimal-editor summary.
They remain Stage 1 evidence until explicitly promoted elsewhere.

## Core Primitive Terms
**Primary**  
Start block or source block that initiates a stack.

**Merge**  
Coordination block that accepts multiple inputs and emits one output according to a merge mode.

**Instruction**  
Execution block that acts after merge resolution in the minimal V1 flow.

## Flow Terms
**Snap-Based Stack Flow**  
Build-time structural system in which blocks can only connect in valid positions according to primitive flow rules.

**Vertical Stack**  
Ordered execution chain running from top to bottom.

**Instruction-Last Rule**  
V1 constraint that places Instruction after Merge in the base stack order.

## Merge Terms
**PRIORITY**  
Topmost non-null input wins.

**JOIN**  
Concatenate inputs.

**OVERRIDE**  
Replace one value with another.

**ECHO**  
Stream values sequentially.

## Definitional Candidates
Primary → Merge → Instruction.  
Merge accepts multiple inputs and outputs one stream.  
Start minimal, then expand.

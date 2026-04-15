# BATCH-127 — Definitions Extract

## Terminology Scope Note
These definitions are extracted from a derived milestone summary.
They remain Stage 1 evidence until explicitly promoted elsewhere.

## Core System Terms
**UMG**  
A specification-first system that defines structured cognition rather than directly executing it.

**Compiler**  
The standalone implementation artifact that deterministically transforms authored UMG structures into RuntimeSpec and Trace.

**Execution**  
External to both the UMG specification layer and the compiler.

## Compiler Identity Terms
**Reference Compiler**  
The first public standalone implementation artifact positioned as the canonical implementation surface for UMG compilation.

**Headless Compiler**  
A compiler with no UI, no framework bindings, and no opinionated runtime.

**compileSleeve**  
The main public compile entrypoint identified in the source.

**CLI**  
A thin I/O wrapper around compiler logic that reads input, invokes compilation, and emits output.

## Structural Input and Output Terms
**Sleeve JSON**  
Primary authored compiler input.

**TriggerState**  
Compilation input concern that may be provided alongside sleeve data.

**RuntimeSpec**  
Final ordered structural output for downstream systems.

**Trace**  
Forensic record of how and why the compiled structure was produced, including ordering, merge, and rule-application context.

## Packaging and Release Terms
**Project Name**  
Human-facing display identity, here stabilized as UMG Compiler.

**Repo/Package Name**  
Machine-usable repository or package identifier, here stabilized as `umg-compiler`.

**CLI Command**  
Shell command used to invoke the compiler, here stabilized as `umg`.

**Canonical Implementation**  
An implementation explicitly linked from the UMG specification repo as the reference implementation for a framework component.

## Definitional Candidates
UMG defines what cognition is.  
The compiler defines how that cognition is structured.  
Execution remains external.  
The compiler is intentionally headless.  
It only structures cognition.

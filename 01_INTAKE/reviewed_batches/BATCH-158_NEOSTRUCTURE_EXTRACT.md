# BATCH-158 — NeoStructure Extract

## Candidate Integration Structure
The source defines a three-layer integration architecture:

1. Agentic Runner
2. UMG Adapter Layer
3. UMG Kernel

## Kernel Composition
The UMG kernel is defined through:
- MOLT
- CEL
- VSS
- Guards
- Overlays

## Scaffolded File / Folder Structure
- src/runner/*
- src/umg/kernel/*
- src/umg/vault/*
- src/hooks/*
- src/middleware/*
- src/tools/*

## Runtime Structural Pattern
- runner = execution substrate
- adapter = translation / contracts / hooks / middleware
- kernel = planning / control / validation / modulation

## Structural Value
This is strong evidence for a practical runtime bridge between UMG concepts and a host agent system. It also provides a reusable decomposition for future documentation and implementation planning.

## Stage 1 Note
This is a candidate architecture pattern, not a finalized canonical structure.

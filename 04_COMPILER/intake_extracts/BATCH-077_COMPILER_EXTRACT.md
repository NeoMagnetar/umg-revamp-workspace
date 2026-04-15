# BATCH-077 — Compiler Extract

## Scope
Implementation-facing runtime/composition behavior for live Block Manager generation.

## Strong Signals
- Runtime should resolve active blocks by role, not by generic concatenation.
- A lightweight resolver was proposed:
  1. find active Primary
  2. collect active Merge blocks
  3. find active Blueprint
  4. assemble output according to role
- The real app stack implies the logic must fit:
  - React + TypeScript frontend
  - Express + Node backend
  - Drizzle/Zod schema layer
  - current MemStorage persistence

## Candidate Runtime Surfaces
- role-resolution order
- transformation stages
- merge-mode semantics
- client/server orchestration boundary
- instruction editing -> immediate generation preview loop

## Candidate Tasks
- Define deterministic resolution order for Primary, Merge, Blueprint.
- Define whether Binary/ArtOfWar behave as:
  - content payload
  - style modifier
  - transformation pass
- Formalize merge modes:
  - blend
  - dominate
  - reference
- Specify whether generation happens:
  - client-side
  - server-side
  - hybrid coordinated flow

## Compiler Risk
Current semantics are too loose for predictable UI behavior. The batch shows that naive modular blending can visibly fail user intent.

## Confidence
medium

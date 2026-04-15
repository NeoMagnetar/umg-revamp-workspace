# BATCH-171 Definitions Extract

## UMG
A modular cognitive architecture built from interacting block roles rather than a flat prompt.

## Trigger
A dynamic activator that responds to conditions and can activate or deactivate other blocks or directive sets.

## Directive
A higher-order control or strategic layer activated by triggers and used to organize instruction behavior.

## Instruction
An execution-facing action or rule layer, often expressed as tool calls or operational steps.

## Philosophy
A constraint-bearing or biasing layer that shapes reasoning and output. In this batch it is treated as filters and rails rather than a primary control-path block.

## Blueprint
A reusable design-time recipe or scaffolding pattern that maps triggers, directives, and instructions for repeated use.

## Overlay
A horizontal/contextual layer that wraps or filters execution without necessarily defining the main control path.

## Foundation
A lower-level support layer such as memory, IO, or environment dependencies.

## Snap-fit mechanics
The rules governing how blocks connect, including vertical control flow and horizontal contextual attachment.

## Merge priority hierarchy
The precedence rule used when competing block contributions conflict.

## Arbiter
Proposed runtime stage that chooses which triggers fire based on events and context.

## Scheduler
Proposed runtime stage that sequences execution after trigger selection.

## Executor
Proposed runtime stage that performs the resolved instruction set.

## Merger
Proposed runtime stage that combines results, resolves collisions, and enforces constraint-aware conflict handling.

## Auditor
Proposed runtime stage that records path, overlays, conflicts, latency, and other telemetry.

## Filters and rails
Spec-like language for philosophy or ethics layers that constrain execution rather than merely describing values.
